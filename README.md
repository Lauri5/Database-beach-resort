# Beache resort Management System Database

## Overview
This repository contains the design and implementation of a database for managing a lido (beach resort). The system enables customers to reserve access to the lido with various types of services, customizable to their preferences. Equipment availability such as cabins, umbrellas, sunbeds, and pedal boats is limited, and the system tracks their availability and bookings.

## Database Structure

### Tables
1. **Customers**
   - `ID_Cliente` (Primary Key, Fiscal Code)
   - `Nome` (First Name)
   - `Cognome` (Last Name)

2. **Reservations**
   - `ID_Prenotazione` (Primary Key)
   - `Data_Prenotazione` (Reservation Date)
   - `Numero_Ingressi` (Number of Entries)
   - `Costo` (Cost, calculated by entries and selected services)
   - `Periodo` (Period: Daily, Weekly, Biweekly, Monthly, Seasonal)

3. **Payments**
   - `ID_Pagamento` (Primary Key)
   - `Data_Pagamento` (Payment Date)
   - `Importo` (Amount)
   - `Metodo_Pagamento` (Payment Method)

4. **Services**
   - `ID_Servizio` (Primary Key)
   - `Tipo_Dotazione` (Type of Equipment)
   - `Quantita` (Quantity)
   - `Prezzo` (Price)

5. **Equipment Tables (Umbrellas, Cabins, Pedal Boats, Sunbeds)**
   - Each table has:
     - `ID` (Primary Key)
     - `Prenotato` (Booked, Boolean)
     - `Prezzo` (Price)

## Usage

Users can:
- Make reservations through the system interface.
- Check equipment availability.
- View and make payments.

## License

This project is released under the MIT License. See the LICENSE file for more details.

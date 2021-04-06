---
description: Los datos binarios no se pueden insertar en una tabla directamente mediante las consultas INSERT INTO o UPDATE SQL.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Agregar datos binarios a una tabla mediante SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491bfe57354b4faf9f7c385bc4e14c64ad366f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909142"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a>Agregar datos binarios a una tabla mediante SQL

Los datos binarios no se pueden insertar en una tabla directamente mediante las consultas INSERT INTO o UPDATE SQL. Para agregar datos binarios a una tabla, primero debe usar el marcador de parámetro (?) en la consulta como un marcador de posición para el valor binario. La ejecución de la consulta debe incluir un registro que contenga los datos binarios en uno de sus campos.

Un marcador es una referencia de parámetro a un valor proporcionado por un registro enviado con la consulta. Se representa en la instrucción SQL mediante un signo de interrogación (?).

En el siguiente código de ejemplo se agregan datos binarios a una tabla.


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")


int main()  
{ 

PMSIHANDLE hDatabase = 0;
PMSIHANDLE hView = 0;
PMSIHANDLE hRec = 0;

if (ERROR_SUCCESS == MsiOpenDatabase(_T("c:\\temp\\testdb.msi"), MSIDBOPEN_TRANSACT, &hDatabase))
{
    //
    // Open view on Binary table so that we can add a new row, must use '?' to represent Binary data
    //

    if (ERROR_SUCCESS == MsiDatabaseOpenView(hDatabase, _T("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)"), &hView))
    {

        //
        // Create record with binary data in 1st field (must match up with '?' in query)
        //

        hRec = MsiCreateRecord(1);
        if (ERROR_SUCCESS == MsiRecordSetStream(hRec, 1, _T("c:\\temp\\data.bin")))
        {

            //
            // Execute view with record containing binary data value; commit database to save changes
            //

            if (ERROR_SUCCESS == MsiViewExecute(hView, hRec)
              && ERROR_SUCCESS == MsiViewClose(hView)
              && ERROR_SUCCESS == MsiDatabaseCommit(hDatabase))
            {
                //
                // New binary data successfully committed to the database
                //
            }
        }
    }
}

return 0;  
}
```



El siguiente script de ejemplo agrega datos binarios a una tabla.


```VB
Dim Installer
Dim Database
Dim View
Dim Record

Set Installer = CreateObject("WindowsInstaller.Installer")

Set Record = Installer.CreateRecord(1)
Record.SetStream 1, "c:\temp\data.bin"

Set Database = Installer.OpenDatabase("c:\temp\testdb.msi", msiOpenDatabaseModeTransact)
Set View = Database.OpenView("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)")
View.Execute Record
Database.Commit ' save changes
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con consultas](working-with-queries.md)
</dt> <dt>

[Sintaxis de SQL](sql-syntax.md)
</dt> <dt>

[Ejemplos de consultas de base de datos mediante SQL y script](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 




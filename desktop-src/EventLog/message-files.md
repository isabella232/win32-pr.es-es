---
description: Cada origen de evento debe registrar archivos de mensaje que contengan cadenas de descripción para cada identificador de evento, categoría de evento y parámetro.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Archivos de mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44de0c91a098ab1b916a73d99a02d0d31a8b5b7690936322166e65baef4bd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951414"
---
# <a name="message-files"></a>Archivos de mensaje

Cada [origen de eventos](event-sources.md) debe registrar archivos de mensaje que contengan cadenas de descripción para cada identificador [de](event-identifiers.md)evento, categoría [de eventos](event-categories.md)y [parámetro](event-identifiers.md). Registre estos archivos en los valores del Registro **EventMessageFile**, **CategoryMessageFile** y **ParameterMessageFile** para el origen del evento.

Puede crear un archivo de mensaje que contenga descripciones de los identificadores de eventos, categorías y parámetros, o bien crear tres archivos de mensaje independientes. Los identificadores de mensaje de todos los mensajes deben ser únicos tanto si se especifican los mensajes en un archivo como en tres archivos. Varias aplicaciones pueden compartir el mismo archivo de mensaje. Para obtener más información sobre los archivos de mensaje, vea [**Compilador de mensajes**](/windows/desktop/WES/message-compiler--mc-exe-). Para obtener más información sobre la sintaxis de un archivo de mensaje, vea [Archivos de texto de mensaje](message-text-files.md).

## <a name="example-message-file"></a>Archivo de mensaje de ejemplo

A continuación se muestra un archivo de mensaje de ejemplo.

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

La aplicación de visualización de eventos puede usar el procedimiento siguiente para obtener acceso a las [cadenas de mensaje](event-identifiers.md) en el archivo DLL del mensaje.

**Para obtener cadenas de descripción**

1.  Llame a [**la función RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) para abrir el origen del evento.
2.  Llame a [**la función RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para obtener el contenido del valor **EventMessageFile** del origen del evento, que es el nombre del archivo DLL del mensaje.
3.  Llame a [**la función LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para cargar el archivo DLL de mensaje determinado por el paso 2.
4.  Llame a [**la función FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) con el identificador de mensaje para obtener la descripción del archivo DLL. (Tenga en cuenta que los identificadores de mensajes se definen en . Archivo H generado por el compilador de mensajes). La **función FormatMessage** reemplazará las cadenas de inserción con los valores de argumento que pase, pero no reemplazará las cadenas de inserción de parámetros. debe reemplazar las cadenas de inserción de parámetros usted mismo antes de mostrar la cadena.

 

 

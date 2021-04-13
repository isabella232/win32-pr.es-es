---
description: Cada origen de eventos debe registrar archivos de mensajes que contengan cadenas de descripción para cada identificador de evento, categoría de evento y parámetro.
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: Archivos de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545019"
---
# <a name="message-files"></a><span data-ttu-id="99969-103">Archivos de mensajes</span><span class="sxs-lookup"><span data-stu-id="99969-103">Message Files</span></span>

<span data-ttu-id="99969-104">Cada [origen de eventos](event-sources.md) debe registrar archivos de mensajes que contengan cadenas de descripción para cada [identificador de evento](event-identifiers.md), [categoría de evento](event-categories.md)y [parámetro](event-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="99969-104">Each [event source](event-sources.md) should register message files that contain description strings for each [event identifier](event-identifiers.md), [event category](event-categories.md), and [parameter](event-identifiers.md).</span></span> <span data-ttu-id="99969-105">Registre estos archivos en los valores del registro **EventMessageFile**, **CategoryMessageFile** y **ParameterMessageFile** para el origen del evento.</span><span class="sxs-lookup"><span data-stu-id="99969-105">Register these files in the **EventMessageFile**, **CategoryMessageFile**, and **ParameterMessageFile** registry values for the event source.</span></span>

<span data-ttu-id="99969-106">Puede crear un archivo de mensajes que contenga descripciones de los identificadores de eventos, categorías y parámetros, o crear tres archivos de mensajes independientes.</span><span class="sxs-lookup"><span data-stu-id="99969-106">You can create one message file that contains descriptions for the event identifiers, categories, and parameters, or create three separate message files.</span></span> <span data-ttu-id="99969-107">Los identificadores de mensaje para todos los mensajes deben ser únicos si especifica los mensajes en un archivo o en tres archivos.</span><span class="sxs-lookup"><span data-stu-id="99969-107">The message identifiers for all of your messages should be unique whether you specify the messages in one file or three files.</span></span> <span data-ttu-id="99969-108">Varias aplicaciones pueden compartir el mismo archivo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="99969-108">Several applications can share the same message file.</span></span> <span data-ttu-id="99969-109">Para obtener más información sobre los archivos de mensajes, vea [**compilador de mensajes**](/windows/desktop/WES/message-compiler--mc-exe-).</span><span class="sxs-lookup"><span data-stu-id="99969-109">For more information on message files, see [**Message Compiler**](/windows/desktop/WES/message-compiler--mc-exe-).</span></span> <span data-ttu-id="99969-110">Para obtener más información sobre la sintaxis de un archivo de mensaje, consulte [archivos de texto de mensaje](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="99969-110">For details on the syntax of a message file, see [Message Text Files](message-text-files.md).</span></span>

## <a name="example-message-file"></a><span data-ttu-id="99969-111">Archivo de mensaje de ejemplo</span><span class="sxs-lookup"><span data-stu-id="99969-111">Example Message File</span></span>

<span data-ttu-id="99969-112">El siguiente es un archivo de mensaje de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="99969-112">The following is an example message file.</span></span>

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

<span data-ttu-id="99969-113">La aplicación de visualización de eventos puede utilizar el siguiente procedimiento para obtener acceso a las [cadenas de mensaje](event-identifiers.md) en el archivo DLL del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99969-113">The event-viewing application can use the following procedure to gain access to the [message strings](event-identifiers.md) in the message DLL.</span></span>

<span data-ttu-id="99969-114">**Para obtener cadenas de Descripción**</span><span class="sxs-lookup"><span data-stu-id="99969-114">**To obtain description strings**</span></span>

1.  <span data-ttu-id="99969-115">Llame a la función [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) para abrir el origen del evento.</span><span class="sxs-lookup"><span data-stu-id="99969-115">Call the [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) function to open the event source.</span></span>
2.  <span data-ttu-id="99969-116">Llame a la función [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) para obtener el contenido del valor de **EventMessageFile** para el origen del evento, que es el nombre del archivo DLL del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99969-116">Call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function to obtain the contents of the **EventMessageFile** value for the event source, which is the name of the message DLL.</span></span>
3.  <span data-ttu-id="99969-117">Llame a la función [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para cargar el archivo dll de mensaje determinado por el paso 2.</span><span class="sxs-lookup"><span data-stu-id="99969-117">Call the [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) function to load the message DLL determined by step 2.</span></span>
4.  <span data-ttu-id="99969-118">Llame a la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) con el identificador de mensaje para obtener la descripción del archivo dll.</span><span class="sxs-lookup"><span data-stu-id="99969-118">Call the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function with the message identifier to obtain the description from the DLL.</span></span> <span data-ttu-id="99969-119">(Tenga en cuenta que los identificadores de mensajes se definen en. H archivo generado por el compilador de mensajes). La función **FormatMessage** reemplazará las cadenas de inserción usando los valores de argumento que se pasan pero no reemplazará las cadenas de inserción de parámetros; debe reemplazar las cadenas de inserción de parámetros usted mismo antes de mostrar la cadena.</span><span class="sxs-lookup"><span data-stu-id="99969-119">(Note that the messages identifiers are defined in the .H file generated by the message compiler.) The **FormatMessage** function will replace the insertion strings using the argument values that you pass but it will not replace the parameter insertion strings; you must replace the parameter insertion strings yourself before displaying the string.</span></span>

 

 

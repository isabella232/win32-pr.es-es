---
description: Los identificadores de evento identifican de forma única un evento determinado.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificadores de eventos (registro de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543054"
---
# <a name="event-identifiers-event-logging"></a>Identificadores de eventos (registro de eventos)

Los identificadores de evento identifican de forma única un evento determinado. Cada [origen de eventos](event-sources.md) puede definir sus propios eventos numerados y las cadenas de descripción a las que se asignan en su archivo de mensaje. Los visores de eventos pueden presentar estas cadenas al usuario. Deberían ayudar al usuario a entender qué salió mal y sugerir qué acciones debe realizar. Dirija la descripción a los usuarios que resuelvan sus propios problemas, no en los administradores o técnicos de soporte. Para obtener más información, vea [instrucciones de mensajes de error](/windows/desktop/Debug/error-message-guidelines).

## <a name="format"></a>Formato

En el diagrama siguiente se muestra el formato de un identificador de evento.

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Gravedad
</dt> <dd>

Gravedad. La gravedad se define de la siguiente manera:

<dl> <dd>00-correcto</dd> <dd>01: información</dd> <dd>10-ADVERTENCIA</dd> <dd>11-error</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>Unidad
</dt> <dd>

Bit de cliente. Este bit se define de la siguiente manera:

<dl> <dd>0: código del sistema</dd> <dd>1: código de cliente</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>C
</dt> <dd>

Bit reservado.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Instalación
</dt> <dd>

Código de instalación. Este valor puede ser FACILity \_ null.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica
</dt> <dd>

Código de estado de la instalación de.

</dd> </dl>

## <a name="message-definitions"></a>Definiciones de mensaje

Los mensajes se definen en el archivo de mensaje de evento. Las cadenas de Descripción del archivo de mensaje de evento se indizan mediante el identificador de eventos, lo que permite a Visor de eventos Mostrar texto específico del evento para cualquier evento basado en el identificador de eventos. Todas las descripciones están localizadas y dependen del idioma. Para obtener más información sobre cómo compilar un archivo de mensajes, vea [archivos de texto de mensaje](message-text-files.md).

Las cadenas de Descripción pueden contener marcadores de posición de cadena de inserción, con el formato%*n*, donde %1 indica la primera cadena de inserción, etc. Por ejemplo, a continuación se muestra una entrada de ejemplo en el archivo. MC:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

En este caso, el búfer devuelto por [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contiene cadenas de inserción. El miembro **NumStrings** de la estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica el número de cadenas de inserción. El miembro **StringOffset** de la estructura **EVENTLOGRECORD** indica la ubicación de la primera cadena de inserción en el búfer. Puede pasar una matriz de PTRs DWORD \_ que apunte a la dirección de cada cadena del búfer al llamar a la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e insertará las cadenas en el mensaje.

La cadena de Descripción también puede contener marcadores de posición para las cadenas de parámetros del archivo de mensajes de parámetros. Los marcadores de posición tienen el formato%%*n*, donde% %1 se reemplaza por la cadena de parámetro con el identificador de 1, y así sucesivamente. Sin embargo, depende de usted insertar las cadenas de parámetros en la cadena de mensaje que devuelve [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . Normalmente, se llama a **FormatMessage** para obtener la cadena de mensaje del evento. A continuación, analizará la cadena de mensaje para los parámetros%%*n* . Si el mensaje contiene uno o varios parámetros, cargue el valor del registro **ParameterMessageFile** para el origen. Para cada parámetro de la cadena de mensaje, obtenga el identificador y páselo a **FormatMessage** para obtener la cadena de parámetro. Reemplace el parámetro de la cadena de mensaje por la cadena de parámetro devuelta por **FormatMessage** .

## <a name="insertion-strings"></a>Cadenas de inserción

Las cadenas de inserción son cadenas independientes del lenguaje opcionales que se usan para rellenar los valores de los marcadores de posición en las cadenas de descripción. Dado que las cadenas no están localizadas, es fundamental que estos marcadores de posición se usen únicamente para representar cadenas independientes del lenguaje, como valores numéricos, nombres de archivo, nombres de usuario, etc. La longitud de la cadena no debe superar los 32 kilobytes-1 caracteres.

Evite el uso de varias cadenas para crear una descripción más grande. Una cadena de inserción se debe tratar como datos, no como texto. Por ejemplo, en el ejemplo siguiente, pszString1 y pszString2 no se deben usar como cadenas de inserción para pszDescription.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

En el ejemplo siguiente, es adecuado usar pszString1 o pszString2 para la cadena de inserción en pszDescription.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 

---
description: Los identificadores de evento identifican de forma única un evento determinado.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificadores de eventos (registro de eventos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933ef3fafe77a2d0fbc2e62b5b11dd499eb850dc5cb6b2ecdc6c952fe1a3f205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951444"
---
# <a name="event-identifiers-event-logging"></a>Identificadores de eventos (registro de eventos)

Los identificadores de evento identifican de forma única un evento determinado. Cada [origen de](event-sources.md) evento puede definir sus propios eventos numerados y las cadenas de descripción a las que se asignan en su archivo de mensaje. Los visores de eventos pueden presentar estas cadenas al usuario. Deben ayudar al usuario a comprender lo que salió mal y sugerir qué acciones realizar. Dirija la descripción a los usuarios para resolver sus propios problemas, no a los administradores ni a los técnicos de soporte técnico. Para obtener más información, vea [Instrucciones de mensajes de error](/windows/desktop/Debug/error-message-guidelines).

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

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev
</dt> <dd>

Gravedad. La gravedad se define de la siguiente manera:

<dl> <dd>00 - Correcto</dd> <dd>01 - Informativo</dd> <dd>10 - Advertencia</dd> <dd>11 - Error</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>C
</dt> <dd>

Bit de cliente. Este bit se define de la siguiente manera:

<dl> <dd>0 : código del sistema</dd> <dd>1 - Código de cliente</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Bit reservado.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Instalación
</dt> <dd>

Código de la instalación. Este valor puede ser FACILITY \_ NULL.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Código
</dt> <dd>

Código de estado de la instalación.

</dd> </dl>

## <a name="message-definitions"></a>Definiciones de mensaje

Los mensajes se definen en el archivo de mensaje de evento. Las cadenas de descripción del archivo de mensaje de evento se indexa por identificador de evento, lo que permite a Visor de eventos mostrar texto específico del evento para cualquier evento basado en el identificador de evento. Todas las descripciones son localizadas y dependen del idioma. Para obtener más información sobre cómo compilar un archivo de mensaje, vea [Archivos de texto de mensaje](message-text-files.md).

Las cadenas de descripción pueden contener marcadores de posición de cadena de inserción, con el formato %*n*, donde %1 indica la primera cadena de inserción, y así sucesivamente. Por ejemplo, lo siguiente es una entrada de ejemplo en el archivo .mc:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

En este caso, el búfer devuelto por [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contiene cadenas de inserción. El **miembro NumStrings** de la [**estructura EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica el número de cadenas de inserción. El **miembro StringOffset** de la **estructura EVENTLOGRECORD** indica la ubicación de la primera cadena de inserción en el búfer. Puede pasar una matriz de PTR DWORD que apunten a la dirección de cada cadena del búfer al llamar a la función FormatMessage e insertará las cadenas en \_ el mensaje. [](/windows/desktop/api/winbase/nf-winbase-formatmessage)

La cadena de descripción también puede contener marcadores de posición para las cadenas de parámetro del archivo de mensaje de parámetro. Los marcadores de posición tienen la forma %%*n*, donde %%1 se reemplaza por la cadena de parámetro por el identificador de 1, y así sucesivamente. Sin embargo, es usted el que tiene que insertar las cadenas de parámetro en la cadena de mensaje que [**devuelve FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) Normalmente, se llama **a FormatMessage** para obtener la cadena de mensaje del evento. A continuación, analice la cadena de mensaje para %%*n* parámetros. Si el mensaje contiene uno o varios parámetros, cargue el valor del Registro **ParameterMessageFile** para el origen. Para cada parámetro de la cadena de mensaje, obtenga el identificador y pásello a **FormatMessage** para obtener la cadena del parámetro. Reemplace el parámetro de la cadena de mensaje por la cadena de parámetro devuelta **por FormatMessage.**

## <a name="insertion-strings"></a>Cadenas de inserción

Las cadenas de inserción son cadenas opcionales independientes del lenguaje que se usan para rellenar los valores de los marcadores de posición en las cadenas de descripción. Dado que las cadenas no están localizadas, es fundamental que estos marcadores de posición solo se utilicen para representar cadenas independientes del lenguaje, como valores numéricos, nombres de archivo, nombres de usuario, y así sucesivamente. La longitud de la cadena no debe superar los 32 kilobytes- 1 caracteres.

Evite usar varias cadenas para crear una descripción mayor. Una cadena de inserción debe tratarse como datos, no como texto. Por ejemplo, en el ejemplo siguiente, pszString1 y pszString2 no deben usarse como cadenas de inserción para pszDescription.

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

 

 

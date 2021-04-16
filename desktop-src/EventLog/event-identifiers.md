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
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="4c9f7-103">Identificadores de eventos (registro de eventos)</span><span class="sxs-lookup"><span data-stu-id="4c9f7-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="4c9f7-104">Los identificadores de evento identifican de forma única un evento determinado.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="4c9f7-105">Cada [origen de eventos](event-sources.md) puede definir sus propios eventos numerados y las cadenas de descripción a las que se asignan en su archivo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="4c9f7-106">Los visores de eventos pueden presentar estas cadenas al usuario.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="4c9f7-107">Deberían ayudar al usuario a entender qué salió mal y sugerir qué acciones debe realizar.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="4c9f7-108">Dirija la descripción a los usuarios que resuelvan sus propios problemas, no en los administradores o técnicos de soporte.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="4c9f7-109">Para obtener más información, vea [instrucciones de mensajes de error](/windows/desktop/Debug/error-message-guidelines).</span><span class="sxs-lookup"><span data-stu-id="4c9f7-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="4c9f7-110">Formato</span><span class="sxs-lookup"><span data-stu-id="4c9f7-110">Format</span></span>

<span data-ttu-id="4c9f7-111">En el diagrama siguiente se muestra el formato de un identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="4c9f7-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Gravedad</span><span class="sxs-lookup"><span data-stu-id="4c9f7-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="4c9f7-113">Gravedad.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-113">Severity.</span></span> <span data-ttu-id="4c9f7-114">La gravedad se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4c9f7-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="4c9f7-115">00-correcto</span><span class="sxs-lookup"><span data-stu-id="4c9f7-115">00 - Success</span></span></dd> <dd><span data-ttu-id="4c9f7-116">01: información</span><span class="sxs-lookup"><span data-stu-id="4c9f7-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="4c9f7-117">10-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="4c9f7-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="4c9f7-118">11-error</span><span class="sxs-lookup"><span data-stu-id="4c9f7-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="4c9f7-119"><span id="C"></span><span id="c"></span>Unidad</span><span class="sxs-lookup"><span data-stu-id="4c9f7-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="4c9f7-120">Bit de cliente.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-120">Customer bit.</span></span> <span data-ttu-id="4c9f7-121">Este bit se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4c9f7-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="4c9f7-122">0: código del sistema</span><span class="sxs-lookup"><span data-stu-id="4c9f7-122">0 - System code</span></span></dd> <dd><span data-ttu-id="4c9f7-123">1: código de cliente</span><span class="sxs-lookup"><span data-stu-id="4c9f7-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="4c9f7-124"><span id="R"></span><span id="r"></span>C</span><span class="sxs-lookup"><span data-stu-id="4c9f7-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="4c9f7-125">Bit reservado.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="4c9f7-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Instalación</span><span class="sxs-lookup"><span data-stu-id="4c9f7-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="4c9f7-127">Código de instalación.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-127">Facility code.</span></span> <span data-ttu-id="4c9f7-128">Este valor puede ser FACILity \_ null.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="4c9f7-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Codifica</span><span class="sxs-lookup"><span data-stu-id="4c9f7-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="4c9f7-130">Código de estado de la instalación de.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="4c9f7-131">Definiciones de mensaje</span><span class="sxs-lookup"><span data-stu-id="4c9f7-131">Message Definitions</span></span>

<span data-ttu-id="4c9f7-132">Los mensajes se definen en el archivo de mensaje de evento.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="4c9f7-133">Las cadenas de Descripción del archivo de mensaje de evento se indizan mediante el identificador de eventos, lo que permite a Visor de eventos Mostrar texto específico del evento para cualquier evento basado en el identificador de eventos.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="4c9f7-134">Todas las descripciones están localizadas y dependen del idioma.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="4c9f7-135">Para obtener más información sobre cómo compilar un archivo de mensajes, vea [archivos de texto de mensaje](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="4c9f7-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="4c9f7-136">Las cadenas de Descripción pueden contener marcadores de posición de cadena de inserción, con el formato%*n*, donde %1 indica la primera cadena de inserción, etc.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="4c9f7-137">Por ejemplo, a continuación se muestra una entrada de ejemplo en el archivo. MC:</span><span class="sxs-lookup"><span data-stu-id="4c9f7-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="4c9f7-138">En este caso, el búfer devuelto por [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contiene cadenas de inserción.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="4c9f7-139">El miembro **NumStrings** de la estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica el número de cadenas de inserción.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="4c9f7-140">El miembro **StringOffset** de la estructura **EVENTLOGRECORD** indica la ubicación de la primera cadena de inserción en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="4c9f7-141">Puede pasar una matriz de PTRs DWORD \_ que apunte a la dirección de cada cadena del búfer al llamar a la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e insertará las cadenas en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="4c9f7-142">La cadena de Descripción también puede contener marcadores de posición para las cadenas de parámetros del archivo de mensajes de parámetros.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="4c9f7-143">Los marcadores de posición tienen el formato%%*n*, donde% %1 se reemplaza por la cadena de parámetro con el identificador de 1, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="4c9f7-144">Sin embargo, depende de usted insertar las cadenas de parámetros en la cadena de mensaje que devuelve [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="4c9f7-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="4c9f7-145">Normalmente, se llama a **FormatMessage** para obtener la cadena de mensaje del evento.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="4c9f7-146">A continuación, analizará la cadena de mensaje para los parámetros%%*n* .</span><span class="sxs-lookup"><span data-stu-id="4c9f7-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="4c9f7-147">Si el mensaje contiene uno o varios parámetros, cargue el valor del registro **ParameterMessageFile** para el origen.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="4c9f7-148">Para cada parámetro de la cadena de mensaje, obtenga el identificador y páselo a **FormatMessage** para obtener la cadena de parámetro.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="4c9f7-149">Reemplace el parámetro de la cadena de mensaje por la cadena de parámetro devuelta por **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="4c9f7-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="4c9f7-150">Cadenas de inserción</span><span class="sxs-lookup"><span data-stu-id="4c9f7-150">Insertion Strings</span></span>

<span data-ttu-id="4c9f7-151">Las cadenas de inserción son cadenas independientes del lenguaje opcionales que se usan para rellenar los valores de los marcadores de posición en las cadenas de descripción.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="4c9f7-152">Dado que las cadenas no están localizadas, es fundamental que estos marcadores de posición se usen únicamente para representar cadenas independientes del lenguaje, como valores numéricos, nombres de archivo, nombres de usuario, etc.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="4c9f7-153">La longitud de la cadena no debe superar los 32 kilobytes-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="4c9f7-154">Evite el uso de varias cadenas para crear una descripción más grande.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="4c9f7-155">Una cadena de inserción se debe tratar como datos, no como texto.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="4c9f7-156">Por ejemplo, en el ejemplo siguiente, pszString1 y pszString2 no se deben usar como cadenas de inserción para pszDescription.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="4c9f7-157">En el ejemplo siguiente, es adecuado usar pszString1 o pszString2 para la cadena de inserción en pszDescription.</span><span class="sxs-lookup"><span data-stu-id="4c9f7-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 

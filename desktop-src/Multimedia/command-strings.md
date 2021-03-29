---
title: Cadenas de comandos
description: Cadenas de comandos
ms.assetid: ca9ca153-f2bf-45ed-84e6-44e86e8efaed
keywords:
- Cadenas de comandos MCI, acerca de
- Cadenas de comandos MCI, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b62013abff091f668a3b045e9f3ca2e8745f0d9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420549"
---
# <a name="command-strings"></a><span data-ttu-id="c2c34-105">Cadenas de comandos</span><span class="sxs-lookup"><span data-stu-id="c2c34-105">Command Strings</span></span>

<span data-ttu-id="c2c34-106">Para enviar un comando de cadena a un dispositivo MCI, utilice la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , que incluye los parámetros para el comando de cadena y un búfer para cualquier información devuelta.</span><span class="sxs-lookup"><span data-stu-id="c2c34-106">To send a string command to an MCI device, use the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function, which includes parameters for the string command and a buffer for any returned information.</span></span>

<span data-ttu-id="c2c34-107">La función **mciSendString** devuelve cero si es correcto.</span><span class="sxs-lookup"><span data-stu-id="c2c34-107">The **mciSendString** function returns zero if successful.</span></span> <span data-ttu-id="c2c34-108">Si se produce un error en la función, la palabra de orden inferior del valor devuelto contiene un código de error.</span><span class="sxs-lookup"><span data-stu-id="c2c34-108">If the function fails, the low-order word of the return value contains an error code.</span></span> <span data-ttu-id="c2c34-109">Este código de error se puede pasar a la función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) para obtener una descripción de texto del error.</span><span class="sxs-lookup"><span data-stu-id="c2c34-109">You can pass this error code to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function to get a text description of the error.</span></span>

## <a name="syntax-of-command-strings"></a><span data-ttu-id="c2c34-110">Sintaxis de las cadenas de comandos</span><span class="sxs-lookup"><span data-stu-id="c2c34-110">Syntax of Command Strings</span></span>

<span data-ttu-id="c2c34-111">Las cadenas de comandos MCI usan una sintaxis de verbo-objeto-modificador coherente.</span><span class="sxs-lookup"><span data-stu-id="c2c34-111">MCI command strings use a consistent verb-object-modifier syntax.</span></span> <span data-ttu-id="c2c34-112">Cada cadena de comandos incluye un comando, un identificador de dispositivo y argumentos de comando.</span><span class="sxs-lookup"><span data-stu-id="c2c34-112">Each command string includes a command, a device identifier, and command arguments.</span></span> <span data-ttu-id="c2c34-113">Los argumentos son opcionales para algunos comandos y son necesarios para otros.</span><span class="sxs-lookup"><span data-stu-id="c2c34-113">Arguments are optional for some commands and required for others.</span></span>

<span data-ttu-id="c2c34-114">Una cadena de comandos tiene el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="c2c34-114">A command string has the following form:</span></span>

<span data-ttu-id="c2c34-115">*argumentos de identificador de dispositivo de comandos \_*</span><span class="sxs-lookup"><span data-stu-id="c2c34-115">*command device\_id arguments*</span></span>

<span data-ttu-id="c2c34-116">Estos componentes contienen la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="c2c34-116">These components contain the following information:</span></span>

-   <span data-ttu-id="c2c34-117">El *comando* especifica un comando MCI, como [**abrir**](open.md), [**cerrar**](close.md)o [**reproducir**](play.md).</span><span class="sxs-lookup"><span data-stu-id="c2c34-117">The *command* specifies an MCI command, such as [**open**](open.md), [**close**](close.md), or [**play**](play.md).</span></span>
-   <span data-ttu-id="c2c34-118">El *\_ identificador de dispositivo* identifica una instancia de un controlador MCI.</span><span class="sxs-lookup"><span data-stu-id="c2c34-118">The *device\_id* identifies an instance of an MCI driver.</span></span> <span data-ttu-id="c2c34-119">El *\_ identificador de dispositivo* se crea al abrir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2c34-119">The *device\_id* is created when the device is opened.</span></span>
-   <span data-ttu-id="c2c34-120">Los *argumentos* especifican las marcas y las variables que usa el comando.</span><span class="sxs-lookup"><span data-stu-id="c2c34-120">The *arguments* specify the flags and variables used by the command.</span></span> <span data-ttu-id="c2c34-121">Las marcas son palabras clave que se reconocen con el comando MCI.</span><span class="sxs-lookup"><span data-stu-id="c2c34-121">Flags are keywords recognized with the MCI command.</span></span> <span data-ttu-id="c2c34-122">Las variables son números o cadenas que se aplican al comando MCI o a la marca.</span><span class="sxs-lookup"><span data-stu-id="c2c34-122">Variables are numbers or strings that apply to the MCI command or flag.</span></span>

    <span data-ttu-id="c2c34-123">Por ejemplo, el comando **Play** usa los argumentos "from *Position* " y "to *Position* " para indicar las posiciones en las que iniciar y finalizar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="c2c34-123">For example, the **play** command uses the arguments "from *position* " and "to *position* " to indicate the positions at which to start and end play.</span></span> <span data-ttu-id="c2c34-124">Puede enumerar las marcas que se usan con un comando en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="c2c34-124">You can list the flags used with a command in any order.</span></span> <span data-ttu-id="c2c34-125">Cuando se usa una marca que tiene una variable asociada, se debe proporcionar un valor para la variable.</span><span class="sxs-lookup"><span data-stu-id="c2c34-125">When you use a flag that has a variable associated with it, you must supply a value for the variable.</span></span>

    <span data-ttu-id="c2c34-126">Los argumentos de comando no especificados (y opcionales) suponen un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c2c34-126">Unspecified (and optional) command arguments assume a default value.</span></span>

<span data-ttu-id="c2c34-127">La función de ejemplo siguiente envía el comando [**Play**](play.md) con las marcas "from" y "to".</span><span class="sxs-lookup"><span data-stu-id="c2c34-127">The following example function sends the [**play**](play.md) command with the "from" and "to" flags.</span></span>


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



## <a name="data-types-for-command-variables"></a><span data-ttu-id="c2c34-128">Tipos de datos para variables de comando</span><span class="sxs-lookup"><span data-stu-id="c2c34-128">Data Types for Command Variables</span></span>

<span data-ttu-id="c2c34-129">Puede usar los siguientes tipos de datos para las variables de una cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="c2c34-129">You can use the following data types for the variables in a command string.</span></span>



| <span data-ttu-id="c2c34-130">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="c2c34-130">**Data type**</span></span>        | <span data-ttu-id="c2c34-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c2c34-131">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2c34-132">Cadenas</span><span class="sxs-lookup"><span data-stu-id="c2c34-132">Strings</span></span>              | <span data-ttu-id="c2c34-133">Los tipos de datos de cadena se delimitan mediante espacios en blanco y Comillas iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="c2c34-133">String data types are delimited by leading and trailing white spaces and quotation marks.</span></span> <span data-ttu-id="c2c34-134">MCI quita las comillas simples de una cadena.</span><span class="sxs-lookup"><span data-stu-id="c2c34-134">MCI removes single quotation marks from a string.</span></span> <span data-ttu-id="c2c34-135">Para colocar una comilla en una cadena, utilice un conjunto de dos comillas en las que desee insertar comillas.</span><span class="sxs-lookup"><span data-stu-id="c2c34-135">To put a quotation mark in a string, use a set of two quotation marks where you want to embed your quotation mark.</span></span> <span data-ttu-id="c2c34-136">Para usar una cadena vacía, use dos comillas separadas por espacios en blanco iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="c2c34-136">To use an empty string, use two quotation marks delimited by leading and trailing white spaces.</span></span> |
| <span data-ttu-id="c2c34-137">Enteros largos con signo</span><span class="sxs-lookup"><span data-stu-id="c2c34-137">Signed long integers</span></span> | <span data-ttu-id="c2c34-138">Los tipos de datos de entero largo con signo se delimitan mediante espacios en blanco iniciales y finales.</span><span class="sxs-lookup"><span data-stu-id="c2c34-138">Signed long integer data types are delimited by leading and trailing white spaces.</span></span> <span data-ttu-id="c2c34-139">A menos que se especifique lo contrario, los enteros pueden ser positivos o negativos.</span><span class="sxs-lookup"><span data-stu-id="c2c34-139">Unless otherwise specified, integers can be positive or negative.</span></span> <span data-ttu-id="c2c34-140">Si usa números enteros negativos, no debe separar el signo menos y el primer dígito con un espacio.</span><span class="sxs-lookup"><span data-stu-id="c2c34-140">If you use negative integers, you should not separate the minus sign and the first digit with a space.</span></span>                                                                                                    |
| <span data-ttu-id="c2c34-141">Rectángulos</span><span class="sxs-lookup"><span data-stu-id="c2c34-141">Rectangles</span></span>           | <span data-ttu-id="c2c34-142">Los tipos de datos de rectángulo son una lista ordenada de cuatro valores cortos firmados.</span><span class="sxs-lookup"><span data-stu-id="c2c34-142">Rectangle data types are an ordered list of four signed short values.</span></span> <span data-ttu-id="c2c34-143">El espacio en blanco delimita este tipo de datos y separa cada entero de la lista.</span><span class="sxs-lookup"><span data-stu-id="c2c34-143">White space delimits this data type and separates each integer in the list.</span></span>                                                                                                                                                                                                              |



 

 

 
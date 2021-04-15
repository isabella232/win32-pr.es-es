---
description: Todo el reconocimiento de controles habilitados para tinta se produce a través de un objeto RecognizerContext. Las API de tecnología de Tablet PC permiten establecer la propiedad Factoid en un objeto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Establecer el contexto para los controles de Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361324"
---
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="5b903-104">Establecer el contexto para los controles de Ink-Enabled</span><span class="sxs-lookup"><span data-stu-id="5b903-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="5b903-105">Todo el reconocimiento de controles habilitados para tinta se produce a través de un objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5b903-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="5b903-106">Las API de tecnología de Tablet PC permiten establecer la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) en un objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="5b903-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="5b903-107">Si va a crear una aplicación habilitada para tinta, utilice las propiedades [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) y de la definición de [**palabras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) del objeto [**RecognizerContext**](inkrecognizercontext-class.md) para establecer contextos.</span><span class="sxs-lookup"><span data-stu-id="5b903-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="5b903-108">Puede pasar los valores de cadena de los nombres de los ámbitos de entrada definidos en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) a la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , delimitados por un carácter de apertura (!</span><span class="sxs-lookup"><span data-stu-id="5b903-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="5b903-109">y un cierre).</span><span class="sxs-lookup"><span data-stu-id="5b903-109">and a closing ).</span></span> <span data-ttu-id="5b903-110">Por ejemplo, para establecer que el contexto de un objeto [**RecognizerContext**](inkrecognizercontext-class.md) se desvíe hacia los caracteres utilizados en una dirección URL, use la sintaxis que se muestra en los siguientes ejemplos de C \# :</span><span class="sxs-lookup"><span data-stu-id="5b903-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="5b903-111">Los ámbitos de entrada que se definen en la enumeración [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reemplazan a los Factoids que estaban disponibles en versiones anteriores del SDK de Windows XP Tablet PC Edition, aunque estos Factoids seguirán funcionando para proporcionar compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="5b903-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="5b903-112">En el siguiente ejemplo de C se \# establece la propiedad [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) para los códigos postales:</span><span class="sxs-lookup"><span data-stu-id="5b903-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="5b903-113">Puede combinar ámbitos de entrada mediante la sintaxis de expresiones regulares de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="5b903-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="5b903-114">Para obtener más información sobre el uso de la sintaxis de expresiones regulares, vea [ámbitos de entrada personalizados con expresiones regulares](custom-input-scopes-with-regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="5b903-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="5b903-115">Puede establecer marcas de reconocimiento en el objeto [**RecognizerContext**](inkrecognizercontext-class.md) para que afecten al comportamiento del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="5b903-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="5b903-116">Una marca de este tipo es la marca de **coerción** en la enumeración [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) del **RecognizerContext**.</span><span class="sxs-lookup"><span data-stu-id="5b903-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="5b903-117">La marca **coerción** obliga al reconocedor a devolver un resultado que coincide con la definición de Factoid que se establece.</span><span class="sxs-lookup"><span data-stu-id="5b903-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="5b903-118">Por ejemplo, si tiene un formulario que requiere que el usuario escriba una cantidad numérica, puede que le resulte útil establecer el **\_ número** Factoid y también establecer la propiedad [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) en **forzar**.</span><span class="sxs-lookup"><span data-stu-id="5b903-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="5b903-119">En esa instancia, la marca **forzar** garantiza que el reconocedor devuelva solo números.</span><span class="sxs-lookup"><span data-stu-id="5b903-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="5b903-120">En el siguiente \# ejemplo de C se establece la propiedad [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) en **coerción**:</span><span class="sxs-lookup"><span data-stu-id="5b903-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="5b903-121">Sin embargo, tenga cuidado al decidir establecer la marca de **coerción** .</span><span class="sxs-lookup"><span data-stu-id="5b903-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="5b903-122">La marca fuerza al reconocedor a que solo coincida con la definición de Factoid.</span><span class="sxs-lookup"><span data-stu-id="5b903-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="5b903-123">Por ejemplo, si establece el ámbito de \_ entrada de teléfono \_ FULLTELEPHONENUMBER y la marca de **coerción** , el reconocedor devuelve resultados que coinciden exactamente con la definición \_ del \_ solo ámbito de entrada de teléfono FULLTELEPHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="5b903-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="5b903-124">Si un usuario escribe "911" con el \_ ámbito de entrada is Phone \_ FULLTELEPHONENUMBER y el indicador de **coerción** establecido, el reconocedor puede devolver una cadena vacía o una cadena aleatoria con el formato (XXX) XXX-XXXX (donde X es un dígito).</span><span class="sxs-lookup"><span data-stu-id="5b903-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="5b903-125">El formato de XXX no coincide con la definición del \_ teléfono \_ FULLTELEPHONENUMBER Factoid, aunque es un número de teléfono válido.</span><span class="sxs-lookup"><span data-stu-id="5b903-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="5b903-126">Para obtener una lista de los formatos admitidos para cada ámbito de entrada, vea la referencia [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .</span><span class="sxs-lookup"><span data-stu-id="5b903-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="5b903-127">Para devolver un campo a la configuración predeterminada del reconocedor, establezca Factoid en es el \_ valor predeterminado, como en el siguiente \# ejemplo de C:</span><span class="sxs-lookup"><span data-stu-id="5b903-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="5b903-128">En el caso de las aplicaciones que utilizan el control [InkEdit](inkedit-control-reference.md) , establezca el tipo Factoid para el control especificando:</span><span class="sxs-lookup"><span data-stu-id="5b903-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="5b903-129">Donde `IS_INPUTSCOPE` es el nombre del ámbito de entrada que desea aplicar.</span><span class="sxs-lookup"><span data-stu-id="5b903-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="5b903-130">El control [InkEdit](inkedit-control-reference.md) no expone un objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5b903-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="5b903-131">Todavía puede asignar el contexto mediante la propiedad [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) del control InkEdit, pero no puede establecer la marca **WORDMODE** .</span><span class="sxs-lookup"><span data-stu-id="5b903-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 

---
title: Propiedad TTSModeID
description: Propiedad TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269238"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="c1df4-103">Propiedad TTSModeID</span><span class="sxs-lookup"><span data-stu-id="c1df4-103">TTSModeID Property</span></span>

<span data-ttu-id="c1df4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1df4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c1df4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="c1df4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c1df4-106">Devuelve o establece el modo del motor TTS utilizado para el carácter.</span><span class="sxs-lookup"><span data-stu-id="c1df4-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="c1df4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="c1df4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c1df4-108">\*agente ***. Caracteres ("*** CharacterID \* *"). TTSModeID* \*  \[  =  *ModeID*\]</span><span class="sxs-lookup"><span data-stu-id="c1df4-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="c1df4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c1df4-109">Part</span></span>     | <span data-ttu-id="c1df4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1df4-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="c1df4-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="c1df4-111">*ModeID*</span></span> | <span data-ttu-id="c1df4-112">Expresión de cadena que corresponde al identificador de modo de un motor de voz.</span><span class="sxs-lookup"><span data-stu-id="c1df4-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1df4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1df4-113">Remarks</span></span>

<span data-ttu-id="c1df4-114">Esta propiedad determina el identificador del modo de motor de TTS (texto a voz) de la salida hablada de un carácter.</span><span class="sxs-lookup"><span data-stu-id="c1df4-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="c1df4-115">El identificador de modo de un motor TTS es una cadena con formato definida por el proveedor de voz que identifica de forma única el modo del motor.</span><span class="sxs-lookup"><span data-stu-id="c1df4-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="c1df4-116">Para obtener más información, consulte [acceso a un motor de voz en el código](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="c1df4-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="c1df4-117">Al establecer esta propiedad, se invalida el intento del servidor de cargar un motor basado en la configuración de TTS compilada del carácter y la configuración de [**LanguageID**](languageid-property.md) actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="c1df4-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="c1df4-118">Sin embargo, si especifica un identificador de modo para un motor que no está instalado o si el usuario ha deshabilitado la salida de voz en la hoja de propiedades del agente de Microsoft (**AudioOutput. Enabled = False**), el servidor genera un error.</span><span class="sxs-lookup"><span data-stu-id="c1df4-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="c1df4-119">Si no se establece (o no correctamente) un identificador de modo TTS para el carácter, el servidor comprueba si la configuración de modo TTS compilado del carácter coincide con la configuración de [**LanguageID**](languageid-property.md) del carácter y si el motor TTS asociado está instalado.</span><span class="sxs-lookup"><span data-stu-id="c1df4-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="c1df4-120">Si es así, el modo TTS utilizado por el carácter para la salida hablada y esta propiedad devuelve ese identificador de modo.</span><span class="sxs-lookup"><span data-stu-id="c1df4-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="c1df4-121">Si no es así, el servidor solicita un motor de voz SAPI compatible que coincida con el **LanguageID** del carácter, así como el sexo y el conjunto de edad para el identificador del modo compilado del carácter.</span><span class="sxs-lookup"><span data-stu-id="c1df4-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="c1df4-122">Si no ha establecido el **ididioma** del carácter, su **LanguageID** es el idioma del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c1df4-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="c1df4-123">Si no se puede encontrar ningún motor coincidente, la consulta de esta propiedad devuelve una cadena vacía para el identificador de modo del motor.</span><span class="sxs-lookup"><span data-stu-id="c1df4-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="c1df4-124">Del mismo modo, si consulta esta propiedad cuando el usuario ha deshabilitado la salida de voz en la hoja de propiedades del agente de Microsoft (**AudioOutput. Enabled = False**), el valor será una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c1df4-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="c1df4-125">Si se consulta o se establece esta propiedad, se cargará el motor asociado (si aún no está cargado).</span><span class="sxs-lookup"><span data-stu-id="c1df4-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="c1df4-126">Sin embargo, si el motor especificado en la configuración de TTS compilada del carácter está instalado y coincide con la configuración de identificador de idioma del carácter, el motor se cargará cuando se cargue el carácter.</span><span class="sxs-lookup"><span data-stu-id="c1df4-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="c1df4-127">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="c1df4-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="c1df4-128">Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="c1df4-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="c1df4-129">Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.</span><span class="sxs-lookup"><span data-stu-id="c1df4-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="c1df4-130">Esta propiedad también devuelve la cadena vacía si no tiene instalado ningún soporte de sonido compatible en el sistema.</span><span class="sxs-lookup"><span data-stu-id="c1df4-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1df4-131">Se puede producir un error en la configuración de **TTSModeID** si no está instalado Speech.dll y el motor especificado no coincide con la configuración de modo TTS compilado del carácter.</span><span class="sxs-lookup"><span data-stu-id="c1df4-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="c1df4-132">Normalmente, la consulta de esta propiedad no devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="c1df4-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="c1df4-133">Sin embargo, si el motor de voz tarda mucho tiempo en cargarse, puede recibir un error que indica que la consulta ha superado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="c1df4-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c1df4-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c1df4-134">See Also</span></span>

[<span data-ttu-id="c1df4-135">**LanguageID (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="c1df4-135">**LanguageID property**</span></span>](languageid-property.md)


 

 





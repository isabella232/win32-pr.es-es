---
title: Propiedad SRModeID
description: Propiedad SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704799"
---
# <a name="srmodeid-property"></a><span data-ttu-id="30fdc-103">Propiedad SRModeID</span><span class="sxs-lookup"><span data-stu-id="30fdc-103">SRModeID Property</span></span>

<span data-ttu-id="30fdc-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30fdc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="30fdc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="30fdc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="30fdc-106">Devuelve o establece el motor de reconocimiento de voz que utiliza el carácter.</span><span class="sxs-lookup"><span data-stu-id="30fdc-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="30fdc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="30fdc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="30fdc-108">\*agente ***. Caracteres ("*** CharacterID \* *"). SRModeID* \*  \[  =  *ModeID*\]</span><span class="sxs-lookup"><span data-stu-id="30fdc-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="30fdc-109">Parte</span><span class="sxs-lookup"><span data-stu-id="30fdc-109">Part</span></span>     | <span data-ttu-id="30fdc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="30fdc-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="30fdc-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="30fdc-111">*ModeID*</span></span> | <span data-ttu-id="30fdc-112">Expresión de cadena que corresponde al identificador de modo de un motor de voz.</span><span class="sxs-lookup"><span data-stu-id="30fdc-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30fdc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30fdc-113">Remarks</span></span>

<span data-ttu-id="30fdc-114">La propiedad determina el motor de reconocimiento de voz usado por el carácter para la entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="30fdc-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="30fdc-115">El identificador de modo de un motor de reconocimiento de voz es una cadena con formato definida por el proveedor de voz que identifica de forma única el motor.</span><span class="sxs-lookup"><span data-stu-id="30fdc-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="30fdc-116">Para obtener más información, consulte [acceso a un motor de voz en el código](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="30fdc-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="30fdc-117">Si especifica un identificador de modo para un motor de voz que no está instalado, si el usuario ha deshabilitado el reconocimiento de voz (en la hoja de propiedades del agente de Microsoft) o si el idioma del motor de voz especificado no coincide con el valor de [**LanguageID**](languageid-property.md) del carácter, el servidor genera un error.</span><span class="sxs-lookup"><span data-stu-id="30fdc-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="30fdc-118">Si consulta esta propiedad y aún no lo ha hecho (correctamente) establecer el motor de reconocimiento de voz, el servidor devuelve el identificador de modo del motor que devuelve SAPI según la configuración de [**LanguageID**](languageid-property.md) del carácter.</span><span class="sxs-lookup"><span data-stu-id="30fdc-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="30fdc-119">Si no ha establecido el **LanguageID** del carácter, el agente devuelve el ID. de modo del motor que SAPI devuelve según la configuración de ID. de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="30fdc-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="30fdc-120">Si no hay ningún motor coincidente, el servidor devuelve una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="30fdc-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="30fdc-121">Al consultar esta propiedad, no es necesario establecer [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) en **true**.</span><span class="sxs-lookup"><span data-stu-id="30fdc-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="30fdc-122">Sin embargo, si consulta la propiedad cuando la entrada de voz está deshabilitada, el servidor devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="30fdc-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="30fdc-123">Cuando se habilita la entrada de voz (en la ventana Opciones de caracteres avanzadas), al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado) y se iniciarán los servicios de voz.</span><span class="sxs-lookup"><span data-stu-id="30fdc-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="30fdc-124">Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible.</span><span class="sxs-lookup"><span data-stu-id="30fdc-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="30fdc-125">(La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.</span><span class="sxs-lookup"><span data-stu-id="30fdc-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="30fdc-126">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="30fdc-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="30fdc-127">Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="30fdc-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="30fdc-128">Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.</span><span class="sxs-lookup"><span data-stu-id="30fdc-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="30fdc-129">Esta propiedad también devuelve la cadena vacía si no tiene instalado ningún soporte de sonido compatible en el sistema.</span><span class="sxs-lookup"><span data-stu-id="30fdc-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="30fdc-130">Normalmente, la consulta de esta propiedad no devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="30fdc-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="30fdc-131">Sin embargo, si el motor de voz tarda mucho tiempo en cargarse, puede recibir un error que indica que la consulta ha superado el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="30fdc-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="30fdc-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="30fdc-132">See Also</span></span>

[<span data-ttu-id="30fdc-133">**LanguageID (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="30fdc-133">**LanguageID property**</span></span>](languageid-property.md)


 

 





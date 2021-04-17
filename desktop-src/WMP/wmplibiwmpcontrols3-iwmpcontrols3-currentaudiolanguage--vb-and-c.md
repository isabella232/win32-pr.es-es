---
title: Propiedad currentAudioLanguage de IWMPControls3
description: La propiedad currentAudioLanguage obtiene o establece el identificador de configuración regional (LCID) del idioma de audio para la reproducción.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- propiedades de currentAudioLanguage Media Player de Windows
- propiedad currentAudioLanguage de Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, propiedad currentAudioLanguage
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709194"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="a5933-106">IWMPControls3:: currentAudioLanguage (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a5933-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="a5933-107">La propiedad **currentAudioLanguage** obtiene o establece el identificador de configuración regional (LCID) del idioma de audio para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a5933-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5933-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5933-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="a5933-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a5933-109">Property value</span></span>

<span data-ttu-id="a5933-110">**System. Int32** que es el LCID del lenguaje de audio.</span><span class="sxs-lookup"><span data-stu-id="a5933-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5933-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5933-111">Remarks</span></span>

<span data-ttu-id="a5933-112">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="a5933-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="a5933-113">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="a5933-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="a5933-114">Al trabajar con contenido de DVD, si se especifica un LCID, se seleccionará la primera pista de audio disponible que tenga el identificador de idioma especificado.</span><span class="sxs-lookup"><span data-stu-id="a5933-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5933-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5933-115">Requirements</span></span>



| <span data-ttu-id="a5933-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5933-116">Requirement</span></span> | <span data-ttu-id="a5933-117">Value</span><span class="sxs-lookup"><span data-stu-id="a5933-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5933-118">Versión</span><span class="sxs-lookup"><span data-stu-id="a5933-118">Version</span></span><br/>   | <span data-ttu-id="a5933-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a5933-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a5933-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5933-120">Namespace</span></span><br/> | <span data-ttu-id="a5933-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a5933-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a5933-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a5933-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a5933-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a5933-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5933-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5933-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5933-125">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5933-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5933-126">**IWMPControls3. audioLanguageCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5933-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5933-127">**IWMPControls3. currentAudioLanguageIndex (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5933-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5933-128">**IWMPControls3. getAudioLanguageDescription (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5933-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5933-129">**IWMPControls3. getAudioLanguageID (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5933-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a5933-130">**IWMPControls3. getLanguageName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a5933-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 






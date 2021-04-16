---
title: IWMPControls3 getAudioLanguageDescription, método
description: El método getAudioLanguageDescription devuelve la descripción del idioma de audio correspondiente al índice basado en uno especificado.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- método getAudioLanguageDescription de Windows Media Player
- método getAudioLanguageDescription Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, método getAudioLanguageDescription
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650139"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="5d230-106">IWMPControls3:: getAudioLanguageDescription (método)</span><span class="sxs-lookup"><span data-stu-id="5d230-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="5d230-107">El método **getAudioLanguageDescription** devuelve la descripción del idioma de audio correspondiente al índice basado en uno especificado.</span><span class="sxs-lookup"><span data-stu-id="5d230-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d230-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d230-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="5d230-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d230-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d230-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5d230-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d230-111">**System. Int32** que es el índice del lenguaje de audio basado en uno.</span><span class="sxs-lookup"><span data-stu-id="5d230-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d230-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d230-112">Return value</span></span>

<span data-ttu-id="5d230-113">**System. String** que es la descripción del lenguaje de audio.</span><span class="sxs-lookup"><span data-stu-id="5d230-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d230-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d230-114">Remarks</span></span>

<span data-ttu-id="5d230-115">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="5d230-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="5d230-116">Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.</span><span class="sxs-lookup"><span data-stu-id="5d230-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d230-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d230-117">Requirements</span></span>



| <span data-ttu-id="5d230-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d230-118">Requirement</span></span> | <span data-ttu-id="5d230-119">Value</span><span class="sxs-lookup"><span data-stu-id="5d230-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d230-120">Versión</span><span class="sxs-lookup"><span data-stu-id="5d230-120">Version</span></span><br/>   | <span data-ttu-id="5d230-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="5d230-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5d230-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d230-122">Namespace</span></span><br/> | <span data-ttu-id="5d230-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5d230-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5d230-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="5d230-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5d230-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5d230-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d230-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d230-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d230-127">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5d230-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d230-128">**IWMPControls3. audioLanguageCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5d230-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d230-129">**IWMPControls3. currentAudioLanguageIndex (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5d230-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d230-130">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5d230-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d230-131">**IWMPControls3. getAudioLanguageID (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5d230-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5d230-132">**IWMPControls3. getLanguageName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="5d230-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 






---
title: Propiedad currentAudioLanguageIndex de IWMPControls3
description: La propiedad currentAudioLanguageIndex obtiene o establece el índice basado en uno que corresponde al lenguaje de audio para la reproducción.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- propiedades de currentAudioLanguageIndex Media Player de Windows
- propiedad currentAudioLanguageIndex de Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, propiedad currentAudioLanguageIndex
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650144"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="ce935-106">IWMPControls3:: currentAudioLanguageIndex (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ce935-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="ce935-107">La propiedad **currentAudioLanguageIndex** obtiene o establece el índice basado en uno que corresponde al lenguaje de audio para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ce935-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce935-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce935-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ce935-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ce935-109">Property value</span></span>

<span data-ttu-id="ce935-110">**System. Int32** que es el índice de base uno del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="ce935-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce935-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce935-111">Remarks</span></span>

<span data-ttu-id="ce935-112">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="ce935-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="ce935-113">Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos.</span><span class="sxs-lookup"><span data-stu-id="ce935-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce935-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce935-114">Requirements</span></span>



| <span data-ttu-id="ce935-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce935-115">Requirement</span></span> | <span data-ttu-id="ce935-116">Value</span><span class="sxs-lookup"><span data-stu-id="ce935-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce935-117">Versión</span><span class="sxs-lookup"><span data-stu-id="ce935-117">Version</span></span><br/>   | <span data-ttu-id="ce935-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ce935-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ce935-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ce935-119">Namespace</span></span><br/> | <span data-ttu-id="ce935-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ce935-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ce935-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ce935-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ce935-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ce935-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce935-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce935-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce935-124">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ce935-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce935-125">**IWMPControls3. audioLanguageCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ce935-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce935-126">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ce935-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce935-127">**IWMPControls3. getAudioLanguageDescription (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ce935-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce935-128">**IWMPControls3. getAudioLanguageID (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ce935-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ce935-129">**IWMPControls3. getLanguageName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ce935-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 






---
title: Propiedad audioLanguageCount de IWMPControls3
description: La propiedad audioLanguageCount obtiene el recuento de idiomas de audio admitidos.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- propiedades de audioLanguageCount Media Player de Windows
- propiedad audioLanguageCount de Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, propiedad audioLanguageCount
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690870"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="dd7df-106">IWMPControls3:: audioLanguageCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dd7df-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="dd7df-107">La propiedad **audioLanguageCount** obtiene el recuento de idiomas de audio admitidos.</span><span class="sxs-lookup"><span data-stu-id="dd7df-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd7df-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd7df-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="dd7df-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dd7df-109">Property value</span></span>

<span data-ttu-id="dd7df-110">**System. Int32** que es el recuento de idiomas de audio admitidos.</span><span class="sxs-lookup"><span data-stu-id="dd7df-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd7df-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd7df-111">Remarks</span></span>

<span data-ttu-id="dd7df-112">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="dd7df-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd7df-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd7df-113">Requirements</span></span>



| <span data-ttu-id="dd7df-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd7df-114">Requirement</span></span> | <span data-ttu-id="dd7df-115">Value</span><span class="sxs-lookup"><span data-stu-id="dd7df-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7df-116">Versión</span><span class="sxs-lookup"><span data-stu-id="dd7df-116">Version</span></span><br/>   | <span data-ttu-id="dd7df-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="dd7df-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dd7df-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd7df-118">Namespace</span></span><br/> | <span data-ttu-id="dd7df-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dd7df-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dd7df-120">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="dd7df-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dd7df-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dd7df-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd7df-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd7df-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd7df-123">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dd7df-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dd7df-124">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dd7df-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dd7df-125">**IWMPControls3. currentAudioLanguageIndex (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dd7df-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dd7df-126">**IWMPControls3. getAudioLanguageDescription (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dd7df-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dd7df-127">**IWMPControls3. getAudioLanguageID (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dd7df-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dd7df-128">**IWMPControls3. getLanguageName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="dd7df-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 






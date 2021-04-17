---
title: Propiedad SAMILangCount de IWMPClosedCaption2
description: La propiedad SAMILangCount obtiene el número de idiomas admitidos por el archivo SAMI actual.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Propiedades de SAMILangCount Media Player de Windows
- Propiedad SAMILangCount de Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, propiedad SAMILangCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690894"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="da618-106">IWMPClosedCaption2:: SAMILangCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="da618-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="da618-107">La propiedad **SAMILangCount** obtiene el número de idiomas admitidos por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="da618-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="da618-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da618-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="da618-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="da618-109">Property value</span></span>

<span data-ttu-id="da618-110">**System. Int32** que es el número de idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="da618-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="da618-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="da618-111">Remarks</span></span>

<span data-ttu-id="da618-112">Esta propiedad devuelve 0 a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="da618-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="da618-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da618-113">Requirements</span></span>



| <span data-ttu-id="da618-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="da618-114">Requirement</span></span> | <span data-ttu-id="da618-115">Value</span><span class="sxs-lookup"><span data-stu-id="da618-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da618-116">Versión</span><span class="sxs-lookup"><span data-stu-id="da618-116">Version</span></span><br/>   | <span data-ttu-id="da618-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="da618-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="da618-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="da618-118">Namespace</span></span><br/> | <span data-ttu-id="da618-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="da618-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="da618-120">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="da618-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="da618-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="da618-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da618-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="da618-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da618-123">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="da618-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="da618-124">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="da618-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da618-125">**IWMPClosedCaption. SAMILang (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="da618-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da618-126">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="da618-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="da618-127">**IWMPClosedCaption2. getSAMILangName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="da618-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 






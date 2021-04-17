---
title: Propiedad SAMIStyleCount de IWMPClosedCaption2
description: La propiedad SAMIStyleCount obtiene el número de estilos admitidos por el archivo SAMI actual.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Propiedades de SAMIStyleCount Media Player de Windows
- Propiedad SAMIStyleCount de Windows Media Player, interfaz IWMPClosedCaption2
- Interfaz IWMPClosedCaption2 Windows Media Player, propiedad SAMIStyleCount
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690892"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a><span data-ttu-id="9b385-106">IWMPClosedCaption2:: SAMIStyleCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9b385-106">IWMPClosedCaption2::SAMIStyleCount property</span></span>

<span data-ttu-id="9b385-107">La propiedad **SAMIStyleCount** obtiene el número de estilos admitidos por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="9b385-107">The **SAMIStyleCount** property gets the number of styles supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b385-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b385-108">Syntax</span></span>


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="9b385-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9b385-109">Property value</span></span>

<span data-ttu-id="9b385-110">**System. Int32** que es el número de estilos.</span><span class="sxs-lookup"><span data-stu-id="9b385-110">A **System.Int32** that is the number of styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b385-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b385-111">Remarks</span></span>

<span data-ttu-id="9b385-112">Esta propiedad devuelve 0 a menos que haya un archivo multimedia digital abierto (AxWindowsMediaPlayer. openState es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="9b385-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b385-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b385-113">Requirements</span></span>



| <span data-ttu-id="9b385-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b385-114">Requirement</span></span> | <span data-ttu-id="9b385-115">Value</span><span class="sxs-lookup"><span data-stu-id="9b385-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b385-116">Versión</span><span class="sxs-lookup"><span data-stu-id="9b385-116">Version</span></span><br/>   | <span data-ttu-id="9b385-117">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9b385-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9b385-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b385-118">Namespace</span></span><br/> | <span data-ttu-id="9b385-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9b385-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9b385-120">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="9b385-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9b385-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9b385-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b385-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b385-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b385-123">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="9b385-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="9b385-124">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9b385-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b385-125">**IWMPClosedCaption. SAMIStyle (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9b385-125">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b385-126">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9b385-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9b385-127">**IWMPClosedCaption2. getSAMIStyleName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9b385-127">**IWMPClosedCaption2.getSAMIStyleName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 






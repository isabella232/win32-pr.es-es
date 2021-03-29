---
title: Propiedad SAMIStyle de IWMPClosedCaption
description: La propiedad SAMIStyle obtiene o establece el estilo de subtítulos (CC).
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Propiedades de SAMIStyle Media Player de Windows
- Propiedad SAMIStyle de Windows Media Player, interfaz IWMPClosedCaption
- Interfaz IWMPClosedCaption Windows Media Player, propiedad SAMIStyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650147"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="d838b-106">IWMPClosedCaption:: SAMIStyle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d838b-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="d838b-107">La propiedad **SAMIStyle** obtiene o establece el estilo de subtítulos (CC).</span><span class="sxs-lookup"><span data-stu-id="d838b-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="d838b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d838b-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="d838b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d838b-109">Property value</span></span>

<span data-ttu-id="d838b-110">**System. String** que es el nombre especificado en el identificador de estilo de un archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="d838b-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="d838b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d838b-111">Remarks</span></span>

<span data-ttu-id="d838b-112">Un archivo SAMI puede contener varias definiciones de estilo de formato.</span><span class="sxs-lookup"><span data-stu-id="d838b-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="d838b-113">Los estilos SAMI se definen entre las etiquetas <STYLE> y </STYLE> del archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="d838b-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="d838b-114">Un estilo se define con una cadena de texto precedida por un \# carácter.</span><span class="sxs-lookup"><span data-stu-id="d838b-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="d838b-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d838b-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="d838b-116">Especifica un estilo que genera una fuente determinada.</span><span class="sxs-lookup"><span data-stu-id="d838b-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="d838b-117">Si no se especifica ningún estilo SAMI, se usa de forma predeterminada el primer estilo definido en el archivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="d838b-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="d838b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d838b-118">Requirements</span></span>



| <span data-ttu-id="d838b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d838b-119">Requirement</span></span> | <span data-ttu-id="d838b-120">Value</span><span class="sxs-lookup"><span data-stu-id="d838b-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d838b-121">Versión</span><span class="sxs-lookup"><span data-stu-id="d838b-121">Version</span></span><br/>   | <span data-ttu-id="d838b-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d838b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d838b-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d838b-123">Namespace</span></span><br/> | <span data-ttu-id="d838b-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d838b-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d838b-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d838b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d838b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d838b-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d838b-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d838b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d838b-128">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="d838b-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="d838b-129">**Interfaz IWMPClosedCaption (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d838b-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d838b-130">**Interfaz IWMPClosedCaption2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d838b-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






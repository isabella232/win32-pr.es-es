---
title: Propiedad de etiqueta IWMPCdromBurn
description: La propiedad etiqueta obtiene la cadena de etiqueta del volumen del CD.
ms.assetid: 46e7741c-59c5-46d8-b9ca-09892d907cd7
keywords:
- propiedades de etiqueta Media Player de Windows
- propiedad etiqueta Media Player Windows, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, propiedad label
topic_type:
- apiref
api_name:
- IWMPCdromBurn.label
- IWMPCdromBurn.get_label
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05da344f1148de7e79cb605135964c6ab8225ac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718828"
---
# <a name="iwmpcdromburnlabel-property"></a><span data-ttu-id="b3f6c-106">IWMPCdromBurn:: Label (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b3f6c-106">IWMPCdromBurn::label property</span></span>

<span data-ttu-id="b3f6c-107">La propiedad *etiqueta* obtiene la cadena de etiqueta del volumen del CD.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-107">The *label* property gets the CD volume label string.</span></span>

<span data-ttu-id="b3f6c-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3f6c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3f6c-109">Syntax</span></span>


```CSharp
public System.String label {get;}
```


```VB

Public ReadOnly Property label As System.String
```





## <a name="property-value"></a><span data-ttu-id="b3f6c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b3f6c-110">Property value</span></span>

<span data-ttu-id="b3f6c-111">**System. String** que es la cadena de la etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-111">A **System.String** that is the volume label string.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3f6c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3f6c-112">Remarks</span></span>

<span data-ttu-id="b3f6c-113">Debido a la forma en que se almacenan las etiquetas de CD, la etiqueta del CD puede ser menor que la longitud de la cadena de etiqueta de volumen especificada.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-113">Due to the way CD labels are stored, the label of the CD may be shorter than the length of the specified volume label string.</span></span> <span data-ttu-id="b3f6c-114">Si la cadena es mayor que la longitud máxima de una etiqueta de CD, se truncará el texto.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-114">If the string is longer than the maximum length of a CD label, the text will be truncated.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3f6c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3f6c-115">Requirements</span></span>



| <span data-ttu-id="b3f6c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3f6c-116">Requirement</span></span> | <span data-ttu-id="b3f6c-117">Value</span><span class="sxs-lookup"><span data-stu-id="b3f6c-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3f6c-118">Versión</span><span class="sxs-lookup"><span data-stu-id="b3f6c-118">Version</span></span><br/>   | <span data-ttu-id="b3f6c-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b3f6c-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b3f6c-120">Namespace</span></span><br/> | <span data-ttu-id="b3f6c-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b3f6c-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b3f6c-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b3f6c-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b3f6c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b3f6c-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3f6c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3f6c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3f6c-125">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b3f6c-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 






---
description: La estructura de \_ bytes con etiqueta define un par de bits con etiqueta. La etiqueta del par de bits con etiqueta se muestra cuando se detecta un valor de propiedad de byte específico.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Estructura de LABELED_BYTE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652881"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="6ade0-104">Estructura de \_ bytes con etiqueta</span><span class="sxs-lookup"><span data-stu-id="6ade0-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="6ade0-105">La estructura de **\_ bytes con etiqueta** define un par de bits con etiqueta.</span><span class="sxs-lookup"><span data-stu-id="6ade0-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="6ade0-106">La **etiqueta** del par de bits con etiqueta se muestra cuando se detecta un valor de propiedad de byte específico.</span><span class="sxs-lookup"><span data-stu-id="6ade0-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ade0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ade0-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="6ade0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ade0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6ade0-109">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6ade0-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="6ade0-110">Valor de BYTE de la propiedad que desea detectar.</span><span class="sxs-lookup"><span data-stu-id="6ade0-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="6ade0-111">**Label**</span><span class="sxs-lookup"><span data-stu-id="6ade0-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="6ade0-112">Descripción o etiqueta textual que se muestra cuando se detecta el valor especificado en el miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="6ade0-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ade0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ade0-113">Remarks</span></span>

<span data-ttu-id="6ade0-114">El miembro **lpLabeledByteTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o más miembros de **etiqueta** de los pares de valor de bytes.</span><span class="sxs-lookup"><span data-stu-id="6ade0-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="6ade0-115">Estos pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de BYTE específico que se encuentra en el paquete del protocolo.</span><span class="sxs-lookup"><span data-stu-id="6ade0-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ade0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ade0-116">Requirements</span></span>



| <span data-ttu-id="6ade0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ade0-117">Requirement</span></span> | <span data-ttu-id="6ade0-118">Value</span><span class="sxs-lookup"><span data-stu-id="6ade0-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ade0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ade0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ade0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6ade0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6ade0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ade0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ade0-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6ade0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6ade0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ade0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ade0-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ade0-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ade0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ade0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ade0-126">SET</span><span class="sxs-lookup"><span data-stu-id="6ade0-126">SET</span></span>](set.md)
</dt> </dl>

 

 





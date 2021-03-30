---
description: La \_ estructura LARGEINT con etiqueta define una etiqueta que se muestra cuando se detecta un valor de propiedad LARGEINT específico.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Estructura de LABELED_LARGEINT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082715"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="7bed5-103">\_Estructura LARGEINT con etiqueta</span><span class="sxs-lookup"><span data-stu-id="7bed5-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="7bed5-104">La estructura **\_ LARGEINT con etiqueta** define una etiqueta que se muestra cuando se detecta un valor de propiedad LARGEINT específico.</span><span class="sxs-lookup"><span data-stu-id="7bed5-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bed5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bed5-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="7bed5-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="7bed5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7bed5-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7bed5-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="7bed5-108">Valor de LARGEINT de la propiedad que desea detectar.</span><span class="sxs-lookup"><span data-stu-id="7bed5-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="7bed5-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="7bed5-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="7bed5-110">Descripción o etiqueta textual que se muestra cuando se detecta el valor de LARGEINT especificado en el miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="7bed5-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bed5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bed5-111">Remarks</span></span>

<span data-ttu-id="7bed5-112">El miembro **lpLabeledLargeIntTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o más miembros de **etiqueta** de los pares de valores LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="7bed5-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="7bed5-113">Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de LARGEINT específico que se encuentra en un paquete de protocolo.</span><span class="sxs-lookup"><span data-stu-id="7bed5-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bed5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bed5-114">Requirements</span></span>



| <span data-ttu-id="7bed5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bed5-115">Requirement</span></span> | <span data-ttu-id="7bed5-116">Value</span><span class="sxs-lookup"><span data-stu-id="7bed5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7bed5-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bed5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7bed5-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7bed5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7bed5-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bed5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7bed5-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bed5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7bed5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bed5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bed5-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bed5-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bed5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bed5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bed5-124">SET</span><span class="sxs-lookup"><span data-stu-id="7bed5-124">SET</span></span>](set.md)
</dt> </dl>

 

 





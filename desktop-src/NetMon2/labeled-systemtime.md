---
description: La \_ estructura SYSTEMTIME con etiqueta define una etiqueta que se muestra cuando se detecta un valor de propiedad SYSTEMTIME específico.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Estructura de LABELED_SYSTEMTIME (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913445"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="495b0-103">\_Estructura SYSTEMTIME con etiqueta</span><span class="sxs-lookup"><span data-stu-id="495b0-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="495b0-104">La estructura **\_ SYSTEMTIME con etiqueta** define una etiqueta que se muestra cuando se detecta un valor de propiedad SYSTEMTIME específico.</span><span class="sxs-lookup"><span data-stu-id="495b0-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="495b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="495b0-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="495b0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="495b0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="495b0-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="495b0-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="495b0-108">Valor SYSTEMTIME de una propiedad que desea detectar.</span><span class="sxs-lookup"><span data-stu-id="495b0-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="495b0-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="495b0-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="495b0-110">Descripción o etiqueta textual que se muestra cuando se detecta el valor SYSTEMTIME especificado en el miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="495b0-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="495b0-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="495b0-111">Remarks</span></span>

<span data-ttu-id="495b0-112">El miembro **lpLabeledSystemTimeTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o varios pares de valores de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="495b0-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="495b0-113">Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de LARGEINT específico que se encuentra en el paquete del protocolo.</span><span class="sxs-lookup"><span data-stu-id="495b0-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="495b0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="495b0-114">Requirements</span></span>



| <span data-ttu-id="495b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="495b0-115">Requirement</span></span> | <span data-ttu-id="495b0-116">Value</span><span class="sxs-lookup"><span data-stu-id="495b0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="495b0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="495b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="495b0-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="495b0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="495b0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="495b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="495b0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="495b0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="495b0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="495b0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="495b0-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="495b0-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495b0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="495b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495b0-124">SET</span><span class="sxs-lookup"><span data-stu-id="495b0-124">SET</span></span>](set.md)
</dt> </dl>

 

 





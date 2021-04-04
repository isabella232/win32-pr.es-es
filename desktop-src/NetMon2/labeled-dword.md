---
description: La \_ estructura DWORD con etiqueta define una etiqueta que se muestra cuando se detecta un valor de propiedad DWORD específico.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Estructura de LABELED_DWORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277977"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="2e5c6-103">\_Estructura DWORD con etiqueta</span><span class="sxs-lookup"><span data-stu-id="2e5c6-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="2e5c6-104">La estructura **\_ DWORD con etiqueta** define una etiqueta que se muestra cuando se detecta un valor de propiedad DWORD específico.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e5c6-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="2e5c6-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e5c6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e5c6-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2e5c6-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="2e5c6-108">Valor DWORD de la propiedad que desea detectar.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="2e5c6-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="2e5c6-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="2e5c6-110">Descripción o etiqueta textual que se muestra cuando se detecta el valor DWORD especificado en el miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="2e5c6-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e5c6-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e5c6-111">Remarks</span></span>

<span data-ttu-id="2e5c6-112">El miembro **lpLabeledDwordTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras **set** que definen uno o más miembros de **etiqueta** de los pares de valores DWORD.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="2e5c6-113">Los pares se usan cuando se desea mostrar una etiqueta en lugar de un valor DWORD específico que se encuentra en el paquete del protocolo.</span><span class="sxs-lookup"><span data-stu-id="2e5c6-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5c6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e5c6-114">Requirements</span></span>



| <span data-ttu-id="2e5c6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5c6-115">Requirement</span></span> | <span data-ttu-id="2e5c6-116">Value</span><span class="sxs-lookup"><span data-stu-id="2e5c6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5c6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e5c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2e5c6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2e5c6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2e5c6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e5c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2e5c6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2e5c6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2e5c6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e5c6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e5c6-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5c6-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e5c6-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e5c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5c6-124">SET</span><span class="sxs-lookup"><span data-stu-id="2e5c6-124">SET</span></span>](set.md)
</dt> </dl>

 

 





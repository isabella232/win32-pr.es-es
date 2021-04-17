---
description: La estructura de \_ palabra etiquetada define una etiqueta que se muestra cuando se detecta un valor de propiedad de Word específico.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Estructura de LABELED_WORD (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678179"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="45d76-103">Estructura de \_ palabras con etiqueta</span><span class="sxs-lookup"><span data-stu-id="45d76-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="45d76-104">La estructura de **\_ palabra etiquetada** define una etiqueta que se muestra cuando se detecta un valor de propiedad de Word específico.</span><span class="sxs-lookup"><span data-stu-id="45d76-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d76-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45d76-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="45d76-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="45d76-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="45d76-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="45d76-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="45d76-108">Valor de palabra de la propiedad que desea detectar.</span><span class="sxs-lookup"><span data-stu-id="45d76-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="45d76-109">**Label**</span><span class="sxs-lookup"><span data-stu-id="45d76-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="45d76-110">Descripción o etiqueta textual que se muestra cuando se detecta el valor de palabra especificado en el miembro de **valor** .</span><span class="sxs-lookup"><span data-stu-id="45d76-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d76-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45d76-111">Remarks</span></span>

<span data-ttu-id="45d76-112">El miembro **lpLabeledWordTable** de la estructura de [conjunto](set.md) apunta a una matriz de estructuras set para definir uno o varios pares de valores de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="45d76-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="45d76-113">Estos pares se usan cuando se desea mostrar una etiqueta en lugar de un valor de palabra específico que se encuentra en un paquete de protocolo.</span><span class="sxs-lookup"><span data-stu-id="45d76-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d76-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d76-114">Requirements</span></span>



| <span data-ttu-id="45d76-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d76-115">Requirement</span></span> | <span data-ttu-id="45d76-116">Value</span><span class="sxs-lookup"><span data-stu-id="45d76-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="45d76-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d76-117">Minimum supported client</span></span><br/> | <span data-ttu-id="45d76-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="45d76-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="45d76-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45d76-119">Minimum supported server</span></span><br/> | <span data-ttu-id="45d76-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="45d76-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="45d76-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="45d76-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="45d76-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="45d76-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d76-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="45d76-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d76-124">SET</span><span class="sxs-lookup"><span data-stu-id="45d76-124">SET</span></span>](set.md)
</dt> </dl>

 

 





---
description: La estructura de \_ bits con etiqueta define un par de bits de etiqueta.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Estructura de LABELED_BIT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652457"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="e656a-103">Estructura de \_ bits con etiqueta</span><span class="sxs-lookup"><span data-stu-id="e656a-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="e656a-104">La estructura de **\_ bits con etiqueta** define un par de bits de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e656a-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="e656a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e656a-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="e656a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e656a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e656a-107">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="e656a-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e656a-108">Número de bits del par de bits de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e656a-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="e656a-109">Los valores oscilan entre 0 y 255.</span><span class="sxs-lookup"><span data-stu-id="e656a-109">Values range from 0 to 255.</span></span> <span data-ttu-id="e656a-110">Establezca el miembro **Bitnumber** en el bit usado en la comparación del valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e656a-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="e656a-111">**LabelOff**</span><span class="sxs-lookup"><span data-stu-id="e656a-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="e656a-112">Cadena o etiqueta que se muestra cuando el BIT especificado en **BitNumber** es igual a cero.</span><span class="sxs-lookup"><span data-stu-id="e656a-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="e656a-113">Por ejemplo, una posible etiqueta es "bit OFF".</span><span class="sxs-lookup"><span data-stu-id="e656a-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="e656a-114">**Etiquetaon**</span><span class="sxs-lookup"><span data-stu-id="e656a-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="e656a-115">Cadena o etiqueta que se muestra cuando el BIT especificado en **BitNumber** es igual a 1.</span><span class="sxs-lookup"><span data-stu-id="e656a-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="e656a-116">Por ejemplo, una posible etiqueta es "bit ON".</span><span class="sxs-lookup"><span data-stu-id="e656a-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e656a-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e656a-117">Remarks</span></span>

<span data-ttu-id="e656a-118">Una matriz de estructuras de **\_ bits con etiqueta** se utiliza para definir un conjunto de pares de bits de etiqueta.</span><span class="sxs-lookup"><span data-stu-id="e656a-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="e656a-119">Un puntero a la matriz se especifica en el miembro **lpLabeledBit** de la estructura [set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="e656a-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="e656a-120">Los pares se usan cuando se desea mostrar una etiqueta basada en la configuración de cada BIT.</span><span class="sxs-lookup"><span data-stu-id="e656a-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="e656a-121">Normalmente, este tipo de conjunto se usa para indicar el valor ON u OFF de BITs.</span><span class="sxs-lookup"><span data-stu-id="e656a-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="e656a-122">Cuando se especifica un conjunto de bits, Monitor de red muestra solo los BITs incluidos en la matriz de estructuras de **conjunto** .</span><span class="sxs-lookup"><span data-stu-id="e656a-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="e656a-123">No se muestran los BITs que no están en la estructura **set** .</span><span class="sxs-lookup"><span data-stu-id="e656a-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e656a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e656a-124">Requirements</span></span>



| <span data-ttu-id="e656a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e656a-125">Requirement</span></span> | <span data-ttu-id="e656a-126">Value</span><span class="sxs-lookup"><span data-stu-id="e656a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e656a-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e656a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e656a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e656a-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e656a-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e656a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e656a-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e656a-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e656a-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e656a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e656a-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e656a-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e656a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e656a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e656a-134">SET</span><span class="sxs-lookup"><span data-stu-id="e656a-134">SET</span></span>](set.md)
</dt> </dl>

 

 





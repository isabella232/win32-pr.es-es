---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY es un tipo que se usa para definir una matriz de revisiones MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905656"
---
# <a name="patcharray"></a><span data-ttu-id="01010-104">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="01010-104">PATCHARRAY</span></span>

<span data-ttu-id="01010-105">PATCHARRAY es un tipo que se usa para definir una matriz de revisiones MIDI.</span><span class="sxs-lookup"><span data-stu-id="01010-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="01010-106">**PATCHARRAY \[ MIDIPATCHSIZE\]**</span><span class="sxs-lookup"><span data-stu-id="01010-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="01010-107">Cada elemento de la matriz corresponde a una revisión con cada uno de los 16 bits que representa uno de los 16 canales MIDI.</span><span class="sxs-lookup"><span data-stu-id="01010-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="01010-108">Los bits se establecen para cada uno de los canales que usan esa revisión concreta.</span><span class="sxs-lookup"><span data-stu-id="01010-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="01010-109">Por ejemplo, si el número de revisión 0 se usa en los canales MIDI físicos 0 y 8, el elemento 0 de la matriz se debe establecer en 0x0101.</span><span class="sxs-lookup"><span data-stu-id="01010-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01010-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01010-110">Requirements</span></span>



| <span data-ttu-id="01010-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="01010-111">Requirement</span></span> | <span data-ttu-id="01010-112">Value</span><span class="sxs-lookup"><span data-stu-id="01010-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01010-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01010-113">Minimum supported client</span></span><br/> | <span data-ttu-id="01010-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="01010-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="01010-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01010-115">Minimum supported server</span></span><br/> | <span data-ttu-id="01010-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01010-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="01010-117">Versión</span><span class="sxs-lookup"><span data-stu-id="01010-117">Version</span></span><br/>                  | <span data-ttu-id="01010-118">Interfaz digital de instrumentos musicales (MIDI), tipos MIDI</span><span class="sxs-lookup"><span data-stu-id="01010-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="01010-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01010-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="01010-120"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01010-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01010-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="01010-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01010-122">Tipos MIDI</span><span class="sxs-lookup"><span data-stu-id="01010-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 






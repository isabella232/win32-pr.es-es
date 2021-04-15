---
title: KEYARRAY (mmsystem. h)
description: KEYARRAY especifica un tipo que se usa para definir una matriz de claves.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676765"
---
# <a name="keyarray"></a><span data-ttu-id="32ebd-104">KEYARRAY</span><span class="sxs-lookup"><span data-stu-id="32ebd-104">KEYARRAY</span></span>

<span data-ttu-id="32ebd-105">KEYARRAY especifica un tipo que se usa para definir una matriz de claves.</span><span class="sxs-lookup"><span data-stu-id="32ebd-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="32ebd-106">**KEYARRAY \[ MIDIPATCHSIZE\]**</span><span class="sxs-lookup"><span data-stu-id="32ebd-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="32ebd-107">Cada elemento de la matriz corresponde a una revisión de percusión basada en claves con cada uno de los 16 bits que representa uno de los 16 canales MIDI.</span><span class="sxs-lookup"><span data-stu-id="32ebd-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="32ebd-108">Los bits se establecen para cada uno de los canales que usan esa revisión concreta.</span><span class="sxs-lookup"><span data-stu-id="32ebd-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="32ebd-109">Por ejemplo, si la revisión de percusión para el número de clave 60 se usa en los canales MIDI físicos 9 y 15, el elemento 60 de la matriz se debe establecer en 0x8200.</span><span class="sxs-lookup"><span data-stu-id="32ebd-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32ebd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32ebd-110">Requirements</span></span>



| <span data-ttu-id="32ebd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ebd-111">Requirement</span></span> | <span data-ttu-id="32ebd-112">Value</span><span class="sxs-lookup"><span data-stu-id="32ebd-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ebd-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32ebd-113">Minimum supported client</span></span><br/> | <span data-ttu-id="32ebd-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32ebd-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="32ebd-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32ebd-115">Minimum supported server</span></span><br/> | <span data-ttu-id="32ebd-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32ebd-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="32ebd-117">Versión</span><span class="sxs-lookup"><span data-stu-id="32ebd-117">Version</span></span><br/>                  | <span data-ttu-id="32ebd-118">Interfaz digital de instrumentos musicales (MIDI), tipos MIDI</span><span class="sxs-lookup"><span data-stu-id="32ebd-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="32ebd-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32ebd-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="32ebd-120"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32ebd-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ebd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="32ebd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ebd-122">Tipos MIDI</span><span class="sxs-lookup"><span data-stu-id="32ebd-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 






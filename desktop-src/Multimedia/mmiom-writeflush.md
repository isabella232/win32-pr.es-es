---
title: Mensaje de MMIOM_WRITEFLUSH (mmsystem. h)
description: La \_ función mmioWrite envía el mensaje WRITEFLUSH MMIOM a un procedimiento de e/s para solicitar que los datos se escriban en un archivo abierto y que los búferes internos utilizados por el procedimiento de e/s se vacíen en el disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- Mensaje de MMIOM_WRITEFLUSH de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803668"
---
# <a name="mmiom_writeflush-message"></a><span data-ttu-id="c4c04-104">MMIOM \_ WRITEFLUSH</span><span class="sxs-lookup"><span data-stu-id="c4c04-104">MMIOM\_WRITEFLUSH message</span></span>

<span data-ttu-id="c4c04-105">La función [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) envía el mensaje **\_ WRITEFLUSH MMIOM** a un procedimiento de e/s para solicitar que los datos se escriban en un archivo abierto y que los búferes internos utilizados por el procedimiento de e/s se vacíen en el disco.</span><span class="sxs-lookup"><span data-stu-id="c4c04-105">The **MMIOM\_WRITEFLUSH** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file and that any internal buffers used by the I/O procedure be flushed to disk.</span></span>


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="c4c04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4c04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c04-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="c4c04-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="c4c04-108">Puntero a un búfer que contiene los datos que se van a escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c4c04-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="c4c04-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="c4c04-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="c4c04-110">Número de bytes que se van a escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c4c04-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c04-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4c04-111">Return Value</span></span>

<span data-ttu-id="c4c04-112">Devuelve el número de bytes realmente escritos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="c4c04-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="c4c04-113">Si hay un error, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="c4c04-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c04-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4c04-114">Remarks</span></span>

<span data-ttu-id="c4c04-115">El procedimiento de e/s es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición de archivo después de la operación de escritura.</span><span class="sxs-lookup"><span data-stu-id="c4c04-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

<span data-ttu-id="c4c04-116">Este mensaje es equivalente al mensaje [**de \_ escritura MMIOM**](mmiom-write.md) , salvo que solicita que el procedimiento de e/s vacíe sus búferes internos, si los hay.</span><span class="sxs-lookup"><span data-stu-id="c4c04-116">This message is equivalent to the [**MMIOM\_WRITE**](mmiom-write.md) message except that it requests that the I/O procedure flush its internal buffers, if any.</span></span> <span data-ttu-id="c4c04-117">A menos que un procedimiento de e/s realice un almacenamiento en búfer interno, este mensaje se puede controlar exactamente como el mensaje de **\_ escritura MMIOM** .</span><span class="sxs-lookup"><span data-stu-id="c4c04-117">Unless an I/O procedure performs internal buffering, this message can be handled exactly like the **MMIOM\_WRITE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c04-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4c04-118">Requirements</span></span>



| <span data-ttu-id="c4c04-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c04-119">Requirement</span></span> | <span data-ttu-id="c4c04-120">Value</span><span class="sxs-lookup"><span data-stu-id="c4c04-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c04-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4c04-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c04-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c4c04-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c4c04-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4c04-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c04-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4c04-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c4c04-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4c04-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c04-126"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c04-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


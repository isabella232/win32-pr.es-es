---
title: Mensaje de MMIOM_SEEK (mmsystem. h)
description: La \_ función mmioSeek envía el mensaje de búsqueda MMIOM a un procedimiento de e/s para solicitar que se mueva la posición del archivo actual.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- Mensaje de MMIOM_SEEK de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686196"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="f60fc-104">MMIOM \_ Buscar mensaje</span><span class="sxs-lookup"><span data-stu-id="f60fc-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="f60fc-105">La función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) envía el mensaje de **\_ búsqueda MMIOM** a un procedimiento de e/s para solicitar que se mueva la posición del archivo actual.</span><span class="sxs-lookup"><span data-stu-id="f60fc-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="f60fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f60fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f60fc-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span><span class="sxs-lookup"><span data-stu-id="f60fc-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="f60fc-108">Nueva posición del archivo.</span><span class="sxs-lookup"><span data-stu-id="f60fc-108">New file position.</span></span> <span data-ttu-id="f60fc-109">El significado de este valor depende de la marca especificada en **lChangeFlag**.</span><span class="sxs-lookup"><span data-stu-id="f60fc-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="f60fc-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span><span class="sxs-lookup"><span data-stu-id="f60fc-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="f60fc-111">Marca que especifica cómo se cambia la posición del archivo.</span><span class="sxs-lookup"><span data-stu-id="f60fc-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="f60fc-112">Se definen los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="f60fc-112">The following values are defined:</span></span>



| <span data-ttu-id="f60fc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f60fc-113">Requirement</span></span> | <span data-ttu-id="f60fc-114">Value</span><span class="sxs-lookup"><span data-stu-id="f60fc-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f60fc-115">BUSCAR \_ CUR</span><span class="sxs-lookup"><span data-stu-id="f60fc-115">SEEK\_CUR</span></span> | <span data-ttu-id="f60fc-116">Mueva la posición del archivo a *lNewFilePos* bytes desde la posición actual.</span><span class="sxs-lookup"><span data-stu-id="f60fc-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="f60fc-117">*lNewFilePos* puede ser positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="f60fc-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="f60fc-118">fin de búsqueda \_</span><span class="sxs-lookup"><span data-stu-id="f60fc-118">SEEK\_END</span></span> | <span data-ttu-id="f60fc-119">Mueva la posición del archivo a *lNewFilePos* bytes desde el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="f60fc-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="f60fc-120">conjunto de búsqueda \_</span><span class="sxs-lookup"><span data-stu-id="f60fc-120">SEEK\_SET</span></span> | <span data-ttu-id="f60fc-121">Mueva la posición del archivo a *lNewFilePos* bytes desde el principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="f60fc-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f60fc-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f60fc-122">Return Value</span></span>

<span data-ttu-id="f60fc-123">Devuelve la nueva posición del archivo.</span><span class="sxs-lookup"><span data-stu-id="f60fc-123">Returns the new file position.</span></span> <span data-ttu-id="f60fc-124">Si hay un error, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="f60fc-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f60fc-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f60fc-125">Remarks</span></span>

<span data-ttu-id="f60fc-126">El procedimiento de e/s es responsable de mantener la posición del archivo actual en el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f60fc-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f60fc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f60fc-127">Requirements</span></span>



| <span data-ttu-id="f60fc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f60fc-128">Requirement</span></span> | <span data-ttu-id="f60fc-129">Value</span><span class="sxs-lookup"><span data-stu-id="f60fc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f60fc-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f60fc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f60fc-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f60fc-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f60fc-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f60fc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f60fc-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f60fc-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f60fc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f60fc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f60fc-135"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f60fc-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


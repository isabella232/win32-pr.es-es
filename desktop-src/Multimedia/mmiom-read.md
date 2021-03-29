---
title: Mensaje de MMIOM_READ (mmsystem. h)
description: La \_ función mmioRead envía el mensaje de lectura MMIOM a un procedimiento de e/s para solicitar que se lea un número especificado de bytes desde un archivo abierto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- Mensaje de MMIOM_READ de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493265"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="cebc3-104">MMIOM \_ leer mensaje</span><span class="sxs-lookup"><span data-stu-id="cebc3-104">MMIOM\_READ message</span></span>

<span data-ttu-id="cebc3-105">La función [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) envía el mensaje de **\_ lectura MMIOM** a un procedimiento de e/s para solicitar que se lea un número especificado de bytes desde un archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="cebc3-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="cebc3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cebc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cebc3-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span><span class="sxs-lookup"><span data-stu-id="cebc3-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="cebc3-108">Puntero al búfer que se va a rellenar con los datos leídos del archivo.</span><span class="sxs-lookup"><span data-stu-id="cebc3-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="cebc3-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span><span class="sxs-lookup"><span data-stu-id="cebc3-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="cebc3-110">Número de bytes que se van a leer del archivo.</span><span class="sxs-lookup"><span data-stu-id="cebc3-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cebc3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cebc3-111">Return Value</span></span>

<span data-ttu-id="cebc3-112">Devuelve el número de bytes realmente leídos del archivo.</span><span class="sxs-lookup"><span data-stu-id="cebc3-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="cebc3-113">Si no se pueden leer más bytes, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="cebc3-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="cebc3-114">Si hay un error, el valor devuelto es 1.</span><span class="sxs-lookup"><span data-stu-id="cebc3-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="cebc3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cebc3-115">Remarks</span></span>

<span data-ttu-id="cebc3-116">El procedimiento de e/s es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición de archivo después de la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="cebc3-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebc3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cebc3-117">Requirements</span></span>



| <span data-ttu-id="cebc3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cebc3-118">Requirement</span></span> | <span data-ttu-id="cebc3-119">Value</span><span class="sxs-lookup"><span data-stu-id="cebc3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cebc3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cebc3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cebc3-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cebc3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cebc3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cebc3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cebc3-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cebc3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cebc3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cebc3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cebc3-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cebc3-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


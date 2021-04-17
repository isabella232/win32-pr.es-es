---
title: Mensaje de MMIOM_OPEN (mmsystem. h)
description: La \_ función mmioOpen envía el mensaje MMIOM Open a un procedimiento de e/s para solicitar que se abra o se elimine un archivo.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- Mensaje de MMIOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651424"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="a3c26-104">MMIOM \_ abrir mensaje</span><span class="sxs-lookup"><span data-stu-id="a3c26-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="a3c26-105">La función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) envía el mensaje **MMIOM \_ Open** a un procedimiento de e/s para solicitar que se abra o se elimine un archivo.</span><span class="sxs-lookup"><span data-stu-id="a3c26-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="a3c26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3c26-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span><span class="sxs-lookup"><span data-stu-id="a3c26-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="a3c26-108">Cadena terminada en null que contiene el nombre del archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="a3c26-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="a3c26-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a3c26-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a3c26-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a3c26-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3c26-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3c26-111">Return Value</span></span>

<span data-ttu-id="a3c26-112">Devuelve MMSYSERR \_ NoError si se realiza correctamente o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a3c26-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="a3c26-113">Entre los posibles valores de error se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3c26-113">Possible error values include the following:</span></span>



| <span data-ttu-id="a3c26-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3c26-114">Requirement</span></span> | <span data-ttu-id="a3c26-115">Value</span><span class="sxs-lookup"><span data-stu-id="a3c26-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="a3c26-116">MMIOM \_ CANNOTOPEN</span><span class="sxs-lookup"><span data-stu-id="a3c26-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="a3c26-117">No se pudo abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="a3c26-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="a3c26-118">MMIOM \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="a3c26-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="a3c26-119">Memoria insuficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="a3c26-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a3c26-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3c26-120">Remarks</span></span>

<span data-ttu-id="a3c26-121">El miembro **dwFlags** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contiene las marcas que se pasan a la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="a3c26-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="a3c26-122">El miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) se inicializa en cero.</span><span class="sxs-lookup"><span data-stu-id="a3c26-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="a3c26-123">Si este valor es incorrecto, el procedimiento de e/s debe corregirlo.</span><span class="sxs-lookup"><span data-stu-id="a3c26-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="a3c26-124">Si la aplicación pasa una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) a [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), el valor devuelto se devuelve en el miembro **wErrorRet** .</span><span class="sxs-lookup"><span data-stu-id="a3c26-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3c26-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3c26-125">Requirements</span></span>



| <span data-ttu-id="a3c26-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3c26-126">Requirement</span></span> | <span data-ttu-id="a3c26-127">Value</span><span class="sxs-lookup"><span data-stu-id="a3c26-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c26-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3c26-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a3c26-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a3c26-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3c26-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3c26-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a3c26-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a3c26-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3c26-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3c26-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3c26-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3c26-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


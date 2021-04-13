---
title: Mensaje de MMIOM_RENAME (mmsystem. h)
description: La \_ función mmioRename envía el mensaje de cambio de nombre MMIOM a un procedimiento de e/s para solicitar que se cambie el nombre del archivo especificado.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- Mensaje de MMIOM_RENAME de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492347"
---
# <a name="mmiom_rename-message"></a><span data-ttu-id="c714d-104">MMIOM \_ cambiar nombre de mensaje</span><span class="sxs-lookup"><span data-stu-id="c714d-104">MMIOM\_RENAME message</span></span>

<span data-ttu-id="c714d-105">La función [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) envía el mensaje de **\_ cambio de nombre MMIOM** a un procedimiento de e/s para solicitar que se cambie el nombre del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="c714d-105">The **MMIOM\_RENAME** message is sent to an I/O procedure by the [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) function to request that the specified file be renamed.</span></span>


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a><span data-ttu-id="c714d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c714d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c714d-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span><span class="sxs-lookup"><span data-stu-id="c714d-107"><span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*</span></span>
</dt> <dd>

<span data-ttu-id="c714d-108">Puntero a una cadena que contiene el nombre del archivo al que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="c714d-108">Pointer to a string containing the filename of the file to rename.</span></span>

</dd> <dt>

<span data-ttu-id="c714d-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span><span class="sxs-lookup"><span data-stu-id="c714d-109"><span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*</span></span>
</dt> <dd>

<span data-ttu-id="c714d-110">Puntero a una cadena que contiene el nuevo nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="c714d-110">Pointer to a string containing the new filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c714d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c714d-111">Return Value</span></span>

<span data-ttu-id="c714d-112">Si se cambia el nombre del archivo correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="c714d-112">If the file is renamed successfully, the return value is zero.</span></span> <span data-ttu-id="c714d-113">Si no se encuentra el archivo especificado, el valor devuelto es MMIOERR \_ FILENOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="c714d-113">If the specified file was not found, the return value is MMIOERR\_FILENOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="c714d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c714d-114">Requirements</span></span>



| <span data-ttu-id="c714d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c714d-115">Requirement</span></span> | <span data-ttu-id="c714d-116">Value</span><span class="sxs-lookup"><span data-stu-id="c714d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c714d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c714d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c714d-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c714d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c714d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c714d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c714d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c714d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c714d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c714d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c714d-122"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c714d-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


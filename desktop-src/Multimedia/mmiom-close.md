---
title: Mensaje de MMIOM_CLOSE (mmsystem. h)
description: La \_ función mmioClose envía el mensaje de cierre MMIOM a un procedimiento de e/s para solicitar que se cierre un archivo.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- Mensaje de MMIOM_CLOSE de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535620"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="461a4-104">MMIOM \_ cerrar mensaje</span><span class="sxs-lookup"><span data-stu-id="461a4-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="461a4-105">La función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) envía el mensaje de **\_ cierre MMIOM** a un procedimiento de e/s para solicitar que se cierre un archivo.</span><span class="sxs-lookup"><span data-stu-id="461a4-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="461a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="461a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="461a4-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span><span class="sxs-lookup"><span data-stu-id="461a4-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="461a4-108">Marcas contenidas en el parámetro **wFlags** de **mmioClose**.</span><span class="sxs-lookup"><span data-stu-id="461a4-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="461a4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="461a4-109">Return Value</span></span>

<span data-ttu-id="461a4-110">Devuelve cero si el archivo se cierra correctamente o si se muestra un error.</span><span class="sxs-lookup"><span data-stu-id="461a4-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="461a4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="461a4-111">Requirements</span></span>



| <span data-ttu-id="461a4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="461a4-112">Requirement</span></span> | <span data-ttu-id="461a4-113">Value</span><span class="sxs-lookup"><span data-stu-id="461a4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="461a4-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="461a4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="461a4-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="461a4-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="461a4-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="461a4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="461a4-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="461a4-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="461a4-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="461a4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="461a4-119"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="461a4-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 


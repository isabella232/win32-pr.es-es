---
title: BG_FILE_RANGE estructura (Deliveryoptimization. h)
description: La estructura BG_FILE_RANGE identifica un intervalo de bytes que se van a descargar de un archivo.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Estructura de BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422530"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="c1255-104">Estructura de BG_FILE_RANGE</span><span class="sxs-lookup"><span data-stu-id="c1255-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="c1255-105">La estructura **BG_FILE_RANGE** identifica un intervalo de bytes que se van a descargar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c1255-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1255-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1255-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="c1255-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c1255-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1255-108">**InitialOffset**</span><span class="sxs-lookup"><span data-stu-id="c1255-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-109">Desplazamiento de base cero al principio del intervalo de bytes que se va a descargar de un archivo.</span><span class="sxs-lookup"><span data-stu-id="c1255-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="c1255-110">**Duración**</span><span class="sxs-lookup"><span data-stu-id="c1255-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="c1255-111">Longitud del intervalo, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c1255-111">The length of the range, in bytes.</span></span> <span data-ttu-id="c1255-112">No especifique una longitud de cero bytes.</span><span class="sxs-lookup"><span data-stu-id="c1255-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="c1255-113">Para indicar que el intervalo se extiende hasta el final del archivo, especifique **BG_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="c1255-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1255-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1255-114">Remarks</span></span>

<span data-ttu-id="c1255-115">El intervalo debe existir en el archivo o generar un error de **DO_E_INVALID_RANGE** .</span><span class="sxs-lookup"><span data-stu-id="c1255-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1255-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1255-116">Requirements</span></span>



| <span data-ttu-id="c1255-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1255-117">Requirement</span></span> | <span data-ttu-id="c1255-118">Value</span><span class="sxs-lookup"><span data-stu-id="c1255-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1255-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1255-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c1255-120">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1255-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1255-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1255-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c1255-122">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="c1255-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c1255-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1255-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1255-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1255-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1255-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1255-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1255-126">**IBackgroundCopyFile2::GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="c1255-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 






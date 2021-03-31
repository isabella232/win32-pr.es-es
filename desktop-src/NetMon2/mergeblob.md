---
description: La función MergeBlob copia todas las entradas del BLOB de origen en un BLOB de destino.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Función MergeBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001234"
---
# <a name="mergeblob-function"></a><span data-ttu-id="28b5e-103">MergeBlob función)</span><span class="sxs-lookup"><span data-stu-id="28b5e-103">MergeBlob function</span></span>

<span data-ttu-id="28b5e-104">La función **MergeBlob** copia todas las entradas del BLOB de origen en un BLOB de destino.</span><span class="sxs-lookup"><span data-stu-id="28b5e-104">The **MergeBlob** function copies all of the entries from the source BLOB into a destination BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28b5e-105">Syntax</span></span>


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a><span data-ttu-id="28b5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28b5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28b5e-107">*hDstBlob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="28b5e-107">*hDstBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28b5e-108">Identificador del BLOB de destino.</span><span class="sxs-lookup"><span data-stu-id="28b5e-108">Handle to the destination BLOB.</span></span> <span data-ttu-id="28b5e-109">En la entrada, este BLOB contiene su información original.</span><span class="sxs-lookup"><span data-stu-id="28b5e-109">On input, this BLOB contains its original information.</span></span> <span data-ttu-id="28b5e-110">En la salida, este BLOB contiene su información original y toda la información del BLOB de origen.</span><span class="sxs-lookup"><span data-stu-id="28b5e-110">On output, this BLOB contains its original information plus all the information of the source BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="28b5e-111">*hSrcBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28b5e-111">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28b5e-112">Identificador del BLOB de origen.</span><span class="sxs-lookup"><span data-stu-id="28b5e-112">Handle to the source BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28b5e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28b5e-113">Return value</span></span>

<span data-ttu-id="28b5e-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="28b5e-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="28b5e-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="28b5e-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b5e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28b5e-116">Remarks</span></span>

<span data-ttu-id="28b5e-117">Las entradas comunes a los archivos de origen y de destino se sobrescribirán con los datos del BLOB de origen.</span><span class="sxs-lookup"><span data-stu-id="28b5e-117">Entries common to source and destination files will be overwritten with data from the source BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="28b5e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28b5e-118">Requirements</span></span>



| <span data-ttu-id="28b5e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="28b5e-119">Requirement</span></span> | <span data-ttu-id="28b5e-120">Value</span><span class="sxs-lookup"><span data-stu-id="28b5e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28b5e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28b5e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28b5e-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28b5e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28b5e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28b5e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28b5e-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28b5e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28b5e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28b5e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="28b5e-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28b5e-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="28b5e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28b5e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="28b5e-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28b5e-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="28b5e-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28b5e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28b5e-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28b5e-130"><dt>Npptools.dll</dt></span></span> </dl> |



 

 





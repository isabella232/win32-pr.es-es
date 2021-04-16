---
description: La función DestroyBlob libera toda la memoria asociada al BLOB y, a continuación, destruye el BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Función DestroyBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669676"
---
# <a name="destroyblob-function"></a><span data-ttu-id="1e27f-103">DestroyBlob función)</span><span class="sxs-lookup"><span data-stu-id="1e27f-103">DestroyBlob function</span></span>

<span data-ttu-id="1e27f-104">La función **DestroyBlob** libera toda la memoria asociada al BLOB y, a continuación, destruye el BLOB.</span><span class="sxs-lookup"><span data-stu-id="1e27f-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e27f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e27f-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1e27f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e27f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e27f-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1e27f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e27f-108">Identificador del objeto al BLOB que se destruye.</span><span class="sxs-lookup"><span data-stu-id="1e27f-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e27f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e27f-109">Return value</span></span>

<span data-ttu-id="1e27f-110">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1e27f-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1e27f-111">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="1e27f-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e27f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e27f-112">Requirements</span></span>



| <span data-ttu-id="1e27f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e27f-113">Requirement</span></span> | <span data-ttu-id="1e27f-114">Value</span><span class="sxs-lookup"><span data-stu-id="1e27f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e27f-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e27f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1e27f-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e27f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1e27f-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e27f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1e27f-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e27f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e27f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e27f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e27f-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e27f-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1e27f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e27f-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="1e27f-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e27f-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1e27f-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e27f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e27f-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e27f-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e27f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e27f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e27f-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="1e27f-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 





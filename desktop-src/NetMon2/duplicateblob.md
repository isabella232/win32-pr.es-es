---
description: La función DuplicateBlob copia un BLOB específico.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: Función DuplicateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652884"
---
# <a name="duplicateblob-function"></a><span data-ttu-id="fed2e-103">DuplicateBlob función)</span><span class="sxs-lookup"><span data-stu-id="fed2e-103">DuplicateBlob function</span></span>

<span data-ttu-id="fed2e-104">La función **DuplicateBlob** copia un BLOB específico.</span><span class="sxs-lookup"><span data-stu-id="fed2e-104">The **DuplicateBlob** function copies a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed2e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fed2e-105">Syntax</span></span>


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="fed2e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fed2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fed2e-107">*hSrcBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fed2e-107">*hSrcBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fed2e-108">Identificador del BLOB que se copia.</span><span class="sxs-lookup"><span data-stu-id="fed2e-108">Handle to the BLOB that is copied.</span></span>

</dd> <dt>

<span data-ttu-id="fed2e-109">*hBlobThatWillBeCreated* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fed2e-109">*hBlobThatWillBeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fed2e-110">Identificador del BLOB duplicado.</span><span class="sxs-lookup"><span data-stu-id="fed2e-110">Handle to the duplicate BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fed2e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fed2e-111">Return value</span></span>

<span data-ttu-id="fed2e-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fed2e-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fed2e-113">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="fed2e-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed2e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fed2e-114">Requirements</span></span>



| <span data-ttu-id="fed2e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fed2e-115">Requirement</span></span> | <span data-ttu-id="fed2e-116">Value</span><span class="sxs-lookup"><span data-stu-id="fed2e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fed2e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fed2e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fed2e-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fed2e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fed2e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fed2e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fed2e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fed2e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fed2e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fed2e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed2e-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fed2e-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="fed2e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fed2e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="fed2e-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fed2e-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="fed2e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fed2e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fed2e-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fed2e-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed2e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fed2e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed2e-128">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="fed2e-128">CreateBlob</span></span>](createblob.md)
</dt> <dt>

[<span data-ttu-id="fed2e-129">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="fed2e-129">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 





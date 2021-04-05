---
description: La función CreateBlob crea un BLOB vacío.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: Función CreateBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: f2abb32afd68dd321a520c1d56c217e801fa9101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814206"
---
# <a name="createblob-function"></a><span data-ttu-id="99710-103">CreateBlob función)</span><span class="sxs-lookup"><span data-stu-id="99710-103">CreateBlob function</span></span>

<span data-ttu-id="99710-104">La función **CreateBlob** crea un BLOB vacío.</span><span class="sxs-lookup"><span data-stu-id="99710-104">The **CreateBlob** function creates an empty BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="99710-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99710-105">Syntax</span></span>


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="99710-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="99710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99710-107">*phBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="99710-107">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99710-108">Puntero a la variable en la que se devuelve el puntero al nuevo BLOB.</span><span class="sxs-lookup"><span data-stu-id="99710-108">Pointer to the variable where the pointer to the new BLOB is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99710-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99710-109">Return value</span></span>

<span data-ttu-id="99710-110">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="99710-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="99710-111">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="99710-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="99710-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99710-112">Requirements</span></span>



| <span data-ttu-id="99710-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="99710-113">Requirement</span></span> | <span data-ttu-id="99710-114">Value</span><span class="sxs-lookup"><span data-stu-id="99710-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99710-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99710-115">Minimum supported client</span></span><br/> | <span data-ttu-id="99710-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="99710-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="99710-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="99710-117">Minimum supported server</span></span><br/> | <span data-ttu-id="99710-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="99710-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99710-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="99710-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="99710-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="99710-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="99710-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99710-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="99710-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99710-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="99710-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="99710-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99710-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99710-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99710-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="99710-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99710-126">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="99710-126">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 





---
description: La función DeleteExtractedFiles elimina los archivos extraídos por la función Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660493"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="6f088-103">DeleteExtractedFiles función)</span><span class="sxs-lookup"><span data-stu-id="6f088-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="6f088-104">\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]</span><span class="sxs-lookup"><span data-stu-id="6f088-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="6f088-105">La función **DeleteExtractedFiles** elimina los archivos extraídos por la función [**Extract**](extract.md) .</span><span class="sxs-lookup"><span data-stu-id="6f088-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f088-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f088-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="6f088-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f088-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f088-108">*PS*</span><span class="sxs-lookup"><span data-stu-id="6f088-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="6f088-109">Puntero a una estructura de [**sesión**](session.md) que contiene información sobre la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="6f088-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="6f088-110">Esta función libera la memoria en el miembro **pFileList** de esta estructura y establece **pFileList** en **null**.</span><span class="sxs-lookup"><span data-stu-id="6f088-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f088-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f088-111">Return value</span></span>

<span data-ttu-id="6f088-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6f088-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f088-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f088-113">Remarks</span></span>

<span data-ttu-id="6f088-114">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6f088-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f088-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f088-115">Requirements</span></span>



| <span data-ttu-id="6f088-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f088-116">Requirement</span></span> | <span data-ttu-id="6f088-117">Value</span><span class="sxs-lookup"><span data-stu-id="6f088-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f088-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f088-118">DLL</span></span><br/> | <dl> <span data-ttu-id="6f088-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f088-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f088-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f088-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f088-121">**Extracción**</span><span class="sxs-lookup"><span data-stu-id="6f088-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="6f088-122">**SESIÓN**</span><span class="sxs-lookup"><span data-stu-id="6f088-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 

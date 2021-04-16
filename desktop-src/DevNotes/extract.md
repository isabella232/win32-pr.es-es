---
description: La función Extract extrae los archivos de un archivo. cab.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extraer función
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649949"
---
# <a name="extract-function"></a><span data-ttu-id="323b7-103">Extraer función</span><span class="sxs-lookup"><span data-stu-id="323b7-103">Extract function</span></span>

<span data-ttu-id="323b7-104">\[Esta función ya no se admite, por lo que no se puede garantizar su comportamiento.\]</span><span class="sxs-lookup"><span data-stu-id="323b7-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="323b7-105">La función **Extract** extrae los archivos de un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="323b7-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="323b7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="323b7-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="323b7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="323b7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="323b7-108">*PS*</span><span class="sxs-lookup"><span data-stu-id="323b7-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="323b7-109">Puntero a una estructura de [**sesión**](session.md) que contiene información sobre la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="323b7-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="323b7-110">*lpCabName*</span><span class="sxs-lookup"><span data-stu-id="323b7-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="323b7-111">Puntero al nombre del archivo. cab del que se van a extraer los archivos.</span><span class="sxs-lookup"><span data-stu-id="323b7-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="323b7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="323b7-112">Return value</span></span>

<span data-ttu-id="323b7-113">Si la función se ejecuta correctamente, devuelve **S \_ OK**; de lo contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="323b7-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="323b7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="323b7-114">Remarks</span></span>

<span data-ttu-id="323b7-115">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="323b7-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="323b7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="323b7-116">Requirements</span></span>



| <span data-ttu-id="323b7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="323b7-117">Requirement</span></span> | <span data-ttu-id="323b7-118">Value</span><span class="sxs-lookup"><span data-stu-id="323b7-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="323b7-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="323b7-119">DLL</span></span><br/> | <dl> <span data-ttu-id="323b7-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="323b7-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="323b7-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="323b7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323b7-122">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="323b7-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="323b7-123">**Fun**</span><span class="sxs-lookup"><span data-stu-id="323b7-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="323b7-124">**SESIÓN**</span><span class="sxs-lookup"><span data-stu-id="323b7-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 

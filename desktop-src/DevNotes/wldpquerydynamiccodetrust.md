---
description: Recupera un valor que determina si la Directiva de Device Guard confía en el código dinámico de la CRL de .NET en memoria o en el disco.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Función WldpQueryDynamicCodeTrust (WLDP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538752"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="b019e-103">WldpQueryDynamicCodeTrust función)</span><span class="sxs-lookup"><span data-stu-id="b019e-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="b019e-104">Recupera un valor que determina si la Directiva de Device Guard confía en el código dinámico de la CRL de .NET en memoria o en el disco.</span><span class="sxs-lookup"><span data-stu-id="b019e-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="b019e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b019e-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="b019e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b019e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b019e-107">*fileHandle*</span><span class="sxs-lookup"><span data-stu-id="b019e-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="b019e-108">Identificador del archivo de código dinámico en disco que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="b019e-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="b019e-109">Si *FILEHANDLE* no es **null**, *baseImage* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b019e-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b019e-110">*baseImage*</span><span class="sxs-lookup"><span data-stu-id="b019e-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="b019e-111">Puntero al archivo PE en memoria que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="b019e-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="b019e-112">Si *baseImage* no es **null**, *FileHandle* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b019e-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b019e-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="b019e-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b019e-114">Cuando *baseImage* no es **null**, indica el tamaño del búfer al que apunta *baseImage* .</span><span class="sxs-lookup"><span data-stu-id="b019e-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b019e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b019e-115">Return value</span></span>

<span data-ttu-id="b019e-116">Este método devuelve **S \_ correcto** si es correcto o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b019e-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b019e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b019e-117">Requirements</span></span>



| <span data-ttu-id="b019e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b019e-118">Requirement</span></span> | <span data-ttu-id="b019e-119">Value</span><span class="sxs-lookup"><span data-stu-id="b019e-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b019e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b019e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b019e-121">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b019e-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b019e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b019e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b019e-123">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="b019e-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b019e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b019e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b019e-125"><dt>WLDP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b019e-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b019e-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b019e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b019e-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b019e-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 





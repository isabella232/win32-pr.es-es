---
description: Convierte los datos de atributos especificados al formato XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906908"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="49464-103">SdbFormatAttribute función)</span><span class="sxs-lookup"><span data-stu-id="49464-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="49464-104">Convierte los datos de atributos especificados al formato XML.</span><span class="sxs-lookup"><span data-stu-id="49464-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="49464-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49464-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="49464-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49464-107">*pAttrInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49464-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49464-108">Estructura [**ATTRINFO**](attrinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="49464-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="49464-109">*pchBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="49464-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49464-110">Búfer de salida.</span><span class="sxs-lookup"><span data-stu-id="49464-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="49464-111">*dwBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49464-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49464-112">Tamaño del búfer de *pchBuffer* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="49464-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49464-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49464-113">Return value</span></span>

<span data-ttu-id="49464-114">La función devuelve **true** si es correcto o **false** si el búfer es demasiado pequeño o no se encuentra el atributo.</span><span class="sxs-lookup"><span data-stu-id="49464-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="49464-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49464-115">Requirements</span></span>



| <span data-ttu-id="49464-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="49464-116">Requirement</span></span> | <span data-ttu-id="49464-117">Value</span><span class="sxs-lookup"><span data-stu-id="49464-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49464-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49464-118">Minimum supported client</span></span><br/> | <span data-ttu-id="49464-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="49464-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="49464-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49464-120">Minimum supported server</span></span><br/> | <span data-ttu-id="49464-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="49464-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="49464-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49464-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49464-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49464-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49464-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="49464-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49464-125">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="49464-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 





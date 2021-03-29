---
description: Libera los datos de atributo de archivo especificados.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806914"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="73b6e-103">SdbFreeFileAttributes función)</span><span class="sxs-lookup"><span data-stu-id="73b6e-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="73b6e-104">Libera los datos de atributo de archivo especificados.</span><span class="sxs-lookup"><span data-stu-id="73b6e-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73b6e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="73b6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73b6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73b6e-107">*pFileAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="73b6e-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73b6e-108">Una estructura [**ATTRINFO**](attrinfo.md) devuelta por la función [**SdbGetFileAttributes**](sdbgetfileattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="73b6e-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73b6e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73b6e-109">Return value</span></span>

<span data-ttu-id="73b6e-110">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="73b6e-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="73b6e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73b6e-111">Requirements</span></span>



| <span data-ttu-id="73b6e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="73b6e-112">Requirement</span></span> | <span data-ttu-id="73b6e-113">Value</span><span class="sxs-lookup"><span data-stu-id="73b6e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73b6e-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73b6e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="73b6e-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="73b6e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73b6e-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="73b6e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="73b6e-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="73b6e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="73b6e-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="73b6e-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73b6e-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73b6e-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b6e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="73b6e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b6e-121">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="73b6e-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 





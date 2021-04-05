---
description: Libera los recursos usados por la función SdbGetMatchingExe.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080151"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="aab78-103">SdbReleaseMatchingExe función)</span><span class="sxs-lookup"><span data-stu-id="aab78-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="aab78-104">Libera los recursos usados por la función [**SdbGetMatchingExe**](sdbgetmatchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="aab78-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="aab78-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aab78-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="aab78-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aab78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab78-107">*hSDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aab78-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aab78-108">Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="aab78-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="aab78-109">*trExe* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aab78-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aab78-110">[**TAGREF**](tagref.md) devuelto por [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span><span class="sxs-lookup"><span data-stu-id="aab78-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab78-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aab78-111">Return value</span></span>

<span data-ttu-id="aab78-112">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="aab78-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab78-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aab78-113">Requirements</span></span>



| <span data-ttu-id="aab78-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aab78-114">Requirement</span></span> | <span data-ttu-id="aab78-115">Value</span><span class="sxs-lookup"><span data-stu-id="aab78-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aab78-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aab78-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aab78-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aab78-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aab78-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aab78-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aab78-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aab78-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aab78-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aab78-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aab78-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aab78-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab78-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="aab78-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab78-123">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="aab78-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="aab78-124">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="aab78-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 





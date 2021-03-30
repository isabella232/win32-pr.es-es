---
description: Cierra la base de datos de correcciones de compatibilidad inicializada con la función SdbInitDatabase.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: SdbReleaseDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538655"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="d7575-103">SdbReleaseDatabase función)</span><span class="sxs-lookup"><span data-stu-id="d7575-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="d7575-104">Cierra la base de datos de correcciones de compatibilidad inicializada con la función [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="d7575-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7575-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7575-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="d7575-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7575-107">*hSDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7575-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7575-108">Identificador de la base de datos de correcciones de compatibilidad (shim) devuelta por la función [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="d7575-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7575-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7575-109">Return value</span></span>

<span data-ttu-id="d7575-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d7575-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7575-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7575-111">Requirements</span></span>



| <span data-ttu-id="d7575-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7575-112">Requirement</span></span> | <span data-ttu-id="d7575-113">Value</span><span class="sxs-lookup"><span data-stu-id="d7575-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7575-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7575-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d7575-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d7575-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7575-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7575-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d7575-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7575-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d7575-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7575-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7575-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7575-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7575-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7575-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7575-121">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="d7575-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 





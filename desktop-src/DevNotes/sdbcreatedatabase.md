---
description: Crea una nueva base de datos de correcciones de compatibilidad.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000578"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="157f7-103">SdbCreateDatabase función)</span><span class="sxs-lookup"><span data-stu-id="157f7-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="157f7-104">Crea una nueva base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="157f7-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="157f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="157f7-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="157f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="157f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="157f7-107">*pwszPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="157f7-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="157f7-108">La ruta de acceso donde debe guardarse la base de datos.</span><span class="sxs-lookup"><span data-stu-id="157f7-108">The path where the database should be saved.</span></span> <span data-ttu-id="157f7-109">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="157f7-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="157f7-110">*ETYPE* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="157f7-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="157f7-111">Tipo de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="157f7-111">The path type.</span></span> <span data-ttu-id="157f7-112">Consulte [**\_ tipo de ruta de acceso**](path-type.md) para obtener una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="157f7-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="157f7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="157f7-113">Return value</span></span>

<span data-ttu-id="157f7-114">La función devuelve un identificador a la base de datos de correcciones de compatibilidad o **null** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="157f7-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="157f7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="157f7-115">Requirements</span></span>



| <span data-ttu-id="157f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="157f7-116">Requirement</span></span> | <span data-ttu-id="157f7-117">Value</span><span class="sxs-lookup"><span data-stu-id="157f7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="157f7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="157f7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="157f7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="157f7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="157f7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="157f7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="157f7-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="157f7-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="157f7-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="157f7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="157f7-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="157f7-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="157f7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="157f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="157f7-125">**SdbOpenDatabase**</span><span class="sxs-lookup"><span data-stu-id="157f7-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 





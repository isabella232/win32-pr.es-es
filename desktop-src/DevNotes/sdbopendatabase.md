---
description: Abre la base de datos de Shim especificada.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807040"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="1112e-103">SdbOpenDatabase función)</span><span class="sxs-lookup"><span data-stu-id="1112e-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="1112e-104">Abre la base de datos de Shim especificada.</span><span class="sxs-lookup"><span data-stu-id="1112e-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1112e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1112e-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="1112e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1112e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1112e-107">*pwszPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1112e-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1112e-108">Ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1112e-108">The database path.</span></span> <span data-ttu-id="1112e-109">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1112e-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1112e-110">*ETYPE* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1112e-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1112e-111">Tipo de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="1112e-111">The path type.</span></span> <span data-ttu-id="1112e-112">Consulte [**\_ tipo de ruta de acceso**](path-type.md) para obtener una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="1112e-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1112e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1112e-113">Return value</span></span>

<span data-ttu-id="1112e-114">La función devuelve un identificador a la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="1112e-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="1112e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1112e-115">Requirements</span></span>



| <span data-ttu-id="1112e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1112e-116">Requirement</span></span> | <span data-ttu-id="1112e-117">Value</span><span class="sxs-lookup"><span data-stu-id="1112e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1112e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1112e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1112e-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1112e-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1112e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1112e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1112e-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1112e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1112e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1112e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1112e-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1112e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="1112e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1112e-125">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="1112e-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 





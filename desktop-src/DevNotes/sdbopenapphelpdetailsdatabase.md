---
description: Abre la base de datos de detalles de apphelp especificada.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152703"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="7f0d6-103">SdbOpenApphelpDetailsDatabase función)</span><span class="sxs-lookup"><span data-stu-id="7f0d6-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="7f0d6-104">Abre la base de datos de detalles de apphelp especificada.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f0d6-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="7f0d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f0d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f0d6-107">*pwsDetailsDatabasePath* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7f0d6-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f0d6-108">Ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-108">The database path.</span></span> <span data-ttu-id="7f0d6-109">Si este parámetro es **null**, se abre la base de datos del sistema local.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f0d6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f0d6-110">Return value</span></span>

<span data-ttu-id="7f0d6-111">La función devuelve un identificador a la base de datos de detalles de apphelp.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0d6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f0d6-112">Requirements</span></span>



| <span data-ttu-id="7f0d6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f0d6-113">Requirement</span></span> | <span data-ttu-id="7f0d6-114">Value</span><span class="sxs-lookup"><span data-stu-id="7f0d6-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0d6-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f0d6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7f0d6-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7f0d6-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7f0d6-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7f0d6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7f0d6-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7f0d6-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7f0d6-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7f0d6-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f0d6-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f0d6-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 





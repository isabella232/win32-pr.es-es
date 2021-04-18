---
description: Recupera el índice de la etiqueta y el tipo de clave especificados de la base de datos especificada.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496175"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="4f042-103">SdbGetIndex función)</span><span class="sxs-lookup"><span data-stu-id="4f042-103">SdbGetIndex function</span></span>

<span data-ttu-id="4f042-104">Recupera el índice de la etiqueta y el tipo de clave especificados de la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="4f042-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f042-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f042-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4f042-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f042-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f042-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f042-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f042-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="4f042-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-109">*tWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f042-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f042-110">ETIQUETA.</span><span class="sxs-lookup"><span data-stu-id="4f042-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-111">*tKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4f042-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f042-112">El tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="4f042-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="4f042-113">*lpdwFlags* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f042-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f042-114">Este parámetro puede ser 0 o **SHIMDB \_ \_ Unique index \_ key** (0x00000001).</span><span class="sxs-lookup"><span data-stu-id="4f042-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f042-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f042-115">Return value</span></span>

<span data-ttu-id="4f042-116">**TagID** del índice o **TagID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="4f042-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f042-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f042-117">Remarks</span></span>

<span data-ttu-id="4f042-118">El índice resultante se puede usar para operaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="4f042-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f042-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f042-119">Requirements</span></span>



| <span data-ttu-id="4f042-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f042-120">Requirement</span></span> | <span data-ttu-id="4f042-121">Value</span><span class="sxs-lookup"><span data-stu-id="4f042-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f042-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f042-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4f042-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4f042-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4f042-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f042-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4f042-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f042-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4f042-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f042-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f042-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f042-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 





---
description: La función DestroyHandoffTable destruye una tabla de entrega creada con CreateHandoffTable.
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Función DestroyHandoffTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001862"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="d9349-103">DestroyHandoffTable función)</span><span class="sxs-lookup"><span data-stu-id="d9349-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="d9349-104">La función **DestroyHandoffTable** destruye una tabla de entrega creada con **CreateHandoffTable**.</span><span class="sxs-lookup"><span data-stu-id="d9349-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9349-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9349-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="d9349-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9349-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9349-107">*hTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d9349-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9349-108">Identificador de la tabla de entrega destruida.</span><span class="sxs-lookup"><span data-stu-id="d9349-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9349-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9349-109">Return value</span></span>

<span data-ttu-id="d9349-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d9349-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9349-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9349-111">Requirements</span></span>



| <span data-ttu-id="d9349-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9349-112">Requirement</span></span> | <span data-ttu-id="d9349-113">Value</span><span class="sxs-lookup"><span data-stu-id="d9349-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9349-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9349-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d9349-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d9349-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d9349-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9349-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d9349-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d9349-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9349-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9349-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9349-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9349-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d9349-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9349-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9349-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9349-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9349-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9349-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9349-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9349-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 





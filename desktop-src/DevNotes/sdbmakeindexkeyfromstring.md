---
description: Crea una clave a partir de una cadena.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998043"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="a75cc-103">SdbMakeIndexKeyFromString función)</span><span class="sxs-lookup"><span data-stu-id="a75cc-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="a75cc-104">Crea una clave a partir de una cadena.</span><span class="sxs-lookup"><span data-stu-id="a75cc-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a75cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a75cc-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="a75cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a75cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a75cc-107">*pwszKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a75cc-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a75cc-108">La cadena.</span><span class="sxs-lookup"><span data-stu-id="a75cc-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a75cc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a75cc-109">Return value</span></span>

<span data-ttu-id="a75cc-110">La función devuelve la clave o 0 si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="a75cc-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a75cc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a75cc-111">Remarks</span></span>

<span data-ttu-id="a75cc-112">La clave de índice estándar son los ocho primeros caracteres de la cadena, convertidos en mayúsculas y, después, se convierten en un valor de **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="a75cc-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a75cc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a75cc-113">Requirements</span></span>



| <span data-ttu-id="a75cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a75cc-114">Requirement</span></span> | <span data-ttu-id="a75cc-115">Value</span><span class="sxs-lookup"><span data-stu-id="a75cc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a75cc-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a75cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a75cc-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a75cc-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a75cc-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a75cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a75cc-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a75cc-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a75cc-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a75cc-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a75cc-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a75cc-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 





---
description: Anula el registro de la base de datos especificada, de modo que ya no está disponible.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496091"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="fa7e1-103">SdbUnregisterDatabase función)</span><span class="sxs-lookup"><span data-stu-id="fa7e1-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="fa7e1-104">Anula el registro de la base de datos especificada, de modo que ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="fa7e1-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa7e1-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="fa7e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa7e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7e1-107">*pguidDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fa7e1-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7e1-108">GUID de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fa7e1-108">The GUID of the database.</span></span> <span data-ttu-id="fa7e1-109">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fa7e1-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7e1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa7e1-110">Return value</span></span>

<span data-ttu-id="fa7e1-111">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="fa7e1-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7e1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa7e1-112">Requirements</span></span>



| <span data-ttu-id="fa7e1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa7e1-113">Requirement</span></span> | <span data-ttu-id="fa7e1-114">Value</span><span class="sxs-lookup"><span data-stu-id="fa7e1-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7e1-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa7e1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fa7e1-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fa7e1-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fa7e1-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa7e1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fa7e1-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa7e1-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fa7e1-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fa7e1-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa7e1-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa7e1-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa7e1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa7e1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7e1-122">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="fa7e1-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 





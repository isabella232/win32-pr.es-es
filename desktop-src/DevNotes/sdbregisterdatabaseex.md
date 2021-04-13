---
description: Registra la base de datos especificada.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538661"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="61b14-103">SdbRegisterDatabaseEx función)</span><span class="sxs-lookup"><span data-stu-id="61b14-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="61b14-104">Registra la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="61b14-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="61b14-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61b14-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="61b14-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61b14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61b14-107">*pszDatabasePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61b14-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61b14-108">Ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="61b14-108">The database path.</span></span> <span data-ttu-id="61b14-109">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="61b14-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="61b14-110">*dwDatabaseType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="61b14-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61b14-111">El tipo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="61b14-111">The database type.</span></span> <span data-ttu-id="61b14-112">Vea [tipos de base de datos de corrección de compatibilidad](shim-database-types.md) para obtener una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="61b14-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="61b14-113">*pTimeStamp* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="61b14-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61b14-114">Marca de tiempo para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="61b14-114">The time stamp for the database.</span></span> <span data-ttu-id="61b14-115">Si este parámetro es **null**, se utiliza la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="61b14-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61b14-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61b14-116">Return value</span></span>

<span data-ttu-id="61b14-117">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="61b14-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="61b14-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61b14-118">Remarks</span></span>

<span data-ttu-id="61b14-119">Se debe registrar una base de datos antes de poder usar cualquier otra función SDB.</span><span class="sxs-lookup"><span data-stu-id="61b14-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="61b14-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61b14-120">Requirements</span></span>



| <span data-ttu-id="61b14-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="61b14-121">Requirement</span></span> | <span data-ttu-id="61b14-122">Value</span><span class="sxs-lookup"><span data-stu-id="61b14-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61b14-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61b14-123">Minimum supported client</span></span><br/> | <span data-ttu-id="61b14-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="61b14-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61b14-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61b14-125">Minimum supported server</span></span><br/> | <span data-ttu-id="61b14-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="61b14-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="61b14-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61b14-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61b14-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61b14-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61b14-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="61b14-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61b14-130">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="61b14-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 





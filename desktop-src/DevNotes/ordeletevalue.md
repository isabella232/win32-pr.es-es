---
description: Quita un valor con nombre de la clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Función ORDeleteValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671487"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="d4e19-103">ORDeleteValue función)</span><span class="sxs-lookup"><span data-stu-id="d4e19-103">ORDeleteValue function</span></span>

<span data-ttu-id="d4e19-104">Quita un valor con nombre de la clave del registro especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d4e19-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4e19-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4e19-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="d4e19-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d4e19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4e19-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d4e19-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e19-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="d4e19-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d4e19-109">*lpValueName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d4e19-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d4e19-110">Valor del registro que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d4e19-110">The registry value to be removed.</span></span> <span data-ttu-id="d4e19-111">Si este parámetro es **null** o una cadena vacía, se quita el valor predeterminado sin nombre establecido por la función [**ORSetValue**](orsetvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e19-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="d4e19-112">Los nombres de valor no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d4e19-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4e19-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d4e19-113">Return value</span></span>

<span data-ttu-id="d4e19-114">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d4e19-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d4e19-115">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d4e19-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="d4e19-116">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="d4e19-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4e19-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4e19-117">Requirements</span></span>



| <span data-ttu-id="d4e19-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4e19-118">Requirement</span></span> | <span data-ttu-id="d4e19-119">Value</span><span class="sxs-lookup"><span data-stu-id="d4e19-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4e19-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d4e19-120">Redistributable</span></span><br/> | <span data-ttu-id="d4e19-121">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="d4e19-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="d4e19-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4e19-122">Header</span></span><br/>          | <dl> <span data-ttu-id="d4e19-123"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4e19-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4e19-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d4e19-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="d4e19-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4e19-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4e19-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4e19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4e19-127">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="d4e19-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 

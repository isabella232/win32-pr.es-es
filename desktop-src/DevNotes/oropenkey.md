---
description: Abre la clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Función OROpenKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650037"
---
# <a name="oropenkey-function"></a><span data-ttu-id="3d208-103">OROpenKey función)</span><span class="sxs-lookup"><span data-stu-id="3d208-103">OROpenKey function</span></span>

<span data-ttu-id="3d208-104">Abre la clave del registro especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3d208-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d208-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d208-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="3d208-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d208-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="3d208-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d208-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3d208-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="3d208-109">*lpSubKeyName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3d208-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3d208-110">Puntero a una cadena Unicode que contiene el nombre de la clave del registro que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="3d208-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="3d208-111">Esta clave debe ser una subclave de la clave identificada por el parámetro de *identificador* .</span><span class="sxs-lookup"><span data-stu-id="3d208-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="3d208-112">Los nombres de clave no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3d208-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="3d208-113">Si este parámetro es **null** o un puntero a una cadena vacía, la función devuelve el mismo identificador que se pasó.</span><span class="sxs-lookup"><span data-stu-id="3d208-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="3d208-114">Si la clave especificada por el parámetro *Handle* es la clave raíz del subárbol, la función devuelve un \_ parámetro de error no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="3d208-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3d208-115">Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="3d208-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d208-116">*phkResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3d208-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d208-117">Puntero a una variable que recibe un identificador de la clave abierta.</span><span class="sxs-lookup"><span data-stu-id="3d208-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="3d208-118">Utilice la función [**ORCloseKey**](orclosekey.md) para cerrar la clave después de haber terminado de usar el identificador.</span><span class="sxs-lookup"><span data-stu-id="3d208-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d208-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d208-119">Return value</span></span>

<span data-ttu-id="3d208-120">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3d208-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3d208-121">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="3d208-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="3d208-122">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="3d208-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="3d208-123">Si el identificador que se va a devolver sería un identificador de la clave raíz del subárbol, la función devuelve un parámetro de ERROR \_ no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="3d208-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="3d208-124">Si la clave especificada se ha marcado como eliminada, esta función devuelve la clave de ERROR \_ \_ eliminada.</span><span class="sxs-lookup"><span data-stu-id="3d208-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d208-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d208-125">Remarks</span></span>

<span data-ttu-id="3d208-126">No se puede usar la función **OROpenKey** para abrir la clave raíz en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="3d208-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="3d208-127">Para obtener un identificador de la clave raíz de un subárbol, use la función [**OROpenHive**](oropenhive.md) para cargar el subárbol en la memoria.</span><span class="sxs-lookup"><span data-stu-id="3d208-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d208-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d208-128">Requirements</span></span>



| <span data-ttu-id="3d208-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d208-129">Requirement</span></span> | <span data-ttu-id="3d208-130">Value</span><span class="sxs-lookup"><span data-stu-id="3d208-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d208-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3d208-131">Redistributable</span></span><br/> | <span data-ttu-id="3d208-132">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3d208-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="3d208-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d208-133">Header</span></span><br/>          | <dl> <span data-ttu-id="3d208-134"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d208-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d208-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d208-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="3d208-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d208-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d208-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d208-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d208-138">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="3d208-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="3d208-139">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="3d208-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="3d208-140">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="3d208-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="3d208-141">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="3d208-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 

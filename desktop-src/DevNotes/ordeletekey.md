---
description: Elimina una subclave y sus valores de un subárbol del registro sin conexión.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Función ORDeleteKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650094"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="8fc00-103">ORDeleteKey función)</span><span class="sxs-lookup"><span data-stu-id="8fc00-103">ORDeleteKey function</span></span>

<span data-ttu-id="8fc00-104">Elimina una subclave y sus valores de un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8fc00-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc00-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fc00-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="8fc00-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fc00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc00-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="8fc00-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc00-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8fc00-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="8fc00-109">Este identificador es devuelto por la función [**ORCreateKey**](orcreatekey.md) o [**OROpenKey**](oropenkey.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc00-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8fc00-110">*lpSubKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8fc00-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc00-111">Nombre de la clave que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8fc00-111">The name of the key to be deleted.</span></span> <span data-ttu-id="8fc00-112">Debe ser una subclave de la clave que *controla* las identificaciones, pero no puede tener subclaves.</span><span class="sxs-lookup"><span data-stu-id="8fc00-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="8fc00-113">Si la subclave no existe, la función devuelve un ERROR \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="8fc00-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="8fc00-114">Si este parámetro es **null**, la función elimina la clave especificada por el parámetro *Handle* .</span><span class="sxs-lookup"><span data-stu-id="8fc00-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="8fc00-115">Si la clave especificada por el parámetro *Handle* es la clave raíz del subárbol, la función devuelve un \_ parámetro de error no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="8fc00-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="8fc00-116">Los nombres de clave no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8fc00-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc00-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fc00-117">Return value</span></span>

<span data-ttu-id="8fc00-118">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8fc00-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8fc00-119">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="8fc00-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="8fc00-120">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="8fc00-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="8fc00-121">Entre los posibles códigos de error se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8fc00-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="8fc00-122">Si la subclave especificada no existe, la función devuelve un \_ archivo de error \_ no \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="8fc00-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="8fc00-123">Si la subclave especificada es la clave raíz del subárbol del registro, la función devuelve un parámetro de ERROR \_ no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="8fc00-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="8fc00-124">Si la subclave especificada tiene subclaves, la función devuelve la clave de ERROR \_ \_ tiene \_ elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="8fc00-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc00-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fc00-125">Remarks</span></span>

<span data-ttu-id="8fc00-126">Si existe la clave del registro especificada, se marca como eliminada.</span><span class="sxs-lookup"><span data-stu-id="8fc00-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="8fc00-127">Una clave eliminada no se quita hasta que se cierra el último identificador de la misma.</span><span class="sxs-lookup"><span data-stu-id="8fc00-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="8fc00-128">La clave que se va a eliminar no debe tener subclaves.</span><span class="sxs-lookup"><span data-stu-id="8fc00-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="8fc00-129">Para eliminar una clave y todas sus subclaves, utilice la función [**OREnumKey**](orenumkey.md) para enumerar las subclaves y eliminarlas de forma individual.</span><span class="sxs-lookup"><span data-stu-id="8fc00-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="8fc00-130">Solo se puede llamar a la función [**ORCloseKey**](orclosekey.md) en una clave eliminada; se produce un error en todas las demás operaciones de registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="8fc00-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="8fc00-131">Si la clave eliminada se creó explícitamente mediante una llamada a [**ORCreateKey**](orcreatekey.md), se liberarán los recursos asociados a la clave cuando se cierre el último identificador de la clave eliminada.</span><span class="sxs-lookup"><span data-stu-id="8fc00-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc00-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc00-132">Requirements</span></span>



| <span data-ttu-id="8fc00-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc00-133">Requirement</span></span> | <span data-ttu-id="8fc00-134">Value</span><span class="sxs-lookup"><span data-stu-id="8fc00-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc00-135">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8fc00-135">Redistributable</span></span><br/> | <span data-ttu-id="8fc00-136">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8fc00-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="8fc00-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8fc00-137">Header</span></span><br/>          | <dl> <span data-ttu-id="8fc00-138"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc00-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fc00-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8fc00-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="8fc00-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc00-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc00-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fc00-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc00-142">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="8fc00-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="8fc00-143">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="8fc00-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="8fc00-144">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="8fc00-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="8fc00-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="8fc00-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 

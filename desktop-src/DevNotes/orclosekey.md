---
description: Cierra un identificador de la clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Función ORCloseKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671490"
---
# <a name="orclosekey-function"></a><span data-ttu-id="1b132-103">ORCloseKey función)</span><span class="sxs-lookup"><span data-stu-id="1b132-103">ORCloseKey function</span></span>

<span data-ttu-id="1b132-104">Cierra un identificador de la clave del registro especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1b132-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b132-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b132-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="1b132-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b132-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1b132-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b132-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1b132-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b132-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b132-109">Return value</span></span>

<span data-ttu-id="1b132-110">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1b132-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1b132-111">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="1b132-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="1b132-112">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="1b132-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="1b132-113">Si la clave especificada es la clave raíz del subárbol del registro, se produce un ERROR en la función con un \_ parámetro no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="1b132-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b132-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b132-114">Remarks</span></span>

<span data-ttu-id="1b132-115">El identificador de una clave especificada no debe usarse una vez que se ha cerrado, porque ya no será válido.</span><span class="sxs-lookup"><span data-stu-id="1b132-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="1b132-116">Los identificadores de clave no deben dejarse abiertos más tiempo del necesario.</span><span class="sxs-lookup"><span data-stu-id="1b132-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="1b132-117">Use la función [**ORCloseHive**](orclosehive.md) para cerrar un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="1b132-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b132-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b132-118">Requirements</span></span>



| <span data-ttu-id="1b132-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b132-119">Requirement</span></span> | <span data-ttu-id="1b132-120">Value</span><span class="sxs-lookup"><span data-stu-id="1b132-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b132-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1b132-121">Redistributable</span></span><br/> | <span data-ttu-id="1b132-122">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1b132-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="1b132-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b132-123">Header</span></span><br/>          | <dl> <span data-ttu-id="1b132-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b132-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b132-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b132-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="1b132-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b132-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b132-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b132-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b132-128">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="1b132-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="1b132-129">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="1b132-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="1b132-130">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="1b132-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="1b132-131">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="1b132-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 

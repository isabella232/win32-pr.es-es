---
description: Cierra el subárbol del registro sin conexión especificado y libera la memoria asignada para el subárbol.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Función ORCloseHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650097"
---
# <a name="orclosehive-function"></a><span data-ttu-id="62c99-103">ORCloseHive función)</span><span class="sxs-lookup"><span data-stu-id="62c99-103">ORCloseHive function</span></span>

<span data-ttu-id="62c99-104">Cierra el subárbol del registro sin conexión especificado y libera la memoria asignada para el subárbol.</span><span class="sxs-lookup"><span data-stu-id="62c99-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c99-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62c99-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="62c99-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c99-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="62c99-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c99-108">Identificador de la clave raíz del subárbol del registro sin conexión que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="62c99-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c99-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62c99-109">Return value</span></span>

<span data-ttu-id="62c99-110">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="62c99-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="62c99-111">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="62c99-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="62c99-112">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="62c99-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c99-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62c99-113">Remarks</span></span>

<span data-ttu-id="62c99-114">La función **ORCloseHive** libera toda la memoria asignada por las funciones del registro sin conexión en nombre del subárbol especificado.</span><span class="sxs-lookup"><span data-stu-id="62c99-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="62c99-115">Para conservar los cambios en el subárbol, llame a la función [**ORSaveHive**](orsavehive.md) antes de llamar a **ORCloseHive**.</span><span class="sxs-lookup"><span data-stu-id="62c99-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c99-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c99-116">Requirements</span></span>



| <span data-ttu-id="62c99-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c99-117">Requirement</span></span> | <span data-ttu-id="62c99-118">Value</span><span class="sxs-lookup"><span data-stu-id="62c99-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62c99-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="62c99-119">Redistributable</span></span><br/> | <span data-ttu-id="62c99-120">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="62c99-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="62c99-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62c99-121">Header</span></span><br/>          | <dl> <span data-ttu-id="62c99-122"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c99-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="62c99-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62c99-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="62c99-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c99-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c99-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="62c99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c99-126">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="62c99-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="62c99-127">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="62c99-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 

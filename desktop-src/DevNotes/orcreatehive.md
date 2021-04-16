---
description: Crea un subárbol del registro sin conexión que contiene una única clave raíz vacía.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Función ORCreateHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650096"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="14635-103">ORCreateHive función)</span><span class="sxs-lookup"><span data-stu-id="14635-103">ORCreateHive function</span></span>

<span data-ttu-id="14635-104">Crea un subárbol del registro sin conexión que contiene una única clave raíz vacía.</span><span class="sxs-lookup"><span data-stu-id="14635-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="14635-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14635-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="14635-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14635-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14635-107">*phkResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="14635-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14635-108">Apunta a una variable para recibir un identificador a la clave raíz del subárbol del registro sin conexión recién creado.</span><span class="sxs-lookup"><span data-stu-id="14635-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="14635-109">Si no se puede crear el subárbol, la función establece este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="14635-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14635-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14635-110">Return value</span></span>

<span data-ttu-id="14635-111">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="14635-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="14635-112">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="14635-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="14635-113">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="14635-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="14635-114">Si no hay memoria suficiente para crear el subárbol del registro, la función devuelve un ERROR que indica que \_ no \_ hay suficiente \_ memoria.</span><span class="sxs-lookup"><span data-stu-id="14635-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="14635-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14635-115">Remarks</span></span>

<span data-ttu-id="14635-116">La función **ORCreateHive** crea un subárbol del registro sin conexión vacío en la memoria.</span><span class="sxs-lookup"><span data-stu-id="14635-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="14635-117">Use las funciones [**ORCreateKey**](orcreatekey.md) y [**ORSetValue**](orsetvalue.md) para agregar claves y establecer sus valores.</span><span class="sxs-lookup"><span data-stu-id="14635-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="14635-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14635-118">Requirements</span></span>



| <span data-ttu-id="14635-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14635-119">Requirement</span></span> | <span data-ttu-id="14635-120">Value</span><span class="sxs-lookup"><span data-stu-id="14635-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14635-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="14635-121">Redistributable</span></span><br/> | <span data-ttu-id="14635-122">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="14635-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="14635-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14635-123">Header</span></span><br/>          | <dl> <span data-ttu-id="14635-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="14635-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="14635-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14635-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="14635-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14635-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14635-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="14635-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14635-128">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="14635-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="14635-129">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="14635-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="14635-130">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="14635-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="14635-131">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="14635-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 

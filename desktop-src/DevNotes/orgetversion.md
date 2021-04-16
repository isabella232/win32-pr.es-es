---
description: Esta función recupera la versión de la biblioteca del registro sin conexión.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Función ORGetVersion (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649849"
---
# <a name="orgetversion-function"></a><span data-ttu-id="97f1e-103">ORGetVersion función)</span><span class="sxs-lookup"><span data-stu-id="97f1e-103">ORGetVersion function</span></span>

<span data-ttu-id="97f1e-104">Esta función recupera la versión de la biblioteca del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="97f1e-104">This function retrieves the version of the offline registry library.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f1e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97f1e-105">Syntax</span></span>


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="97f1e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97f1e-107">*pdwMajorVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-107">*pdwMajorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-108">Un puntero a una variable para recibir la versión principal de la biblioteca del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="97f1e-108">A pointer to a variable to receive the major version of the offline registry library.</span></span> <span data-ttu-id="97f1e-109">Para la versión inicial de la biblioteca, el valor es 1.</span><span class="sxs-lookup"><span data-stu-id="97f1e-109">For the initial release of the library, the value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="97f1e-110">*pdwMinorVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="97f1e-110">*pdwMinorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97f1e-111">Un puntero a una variable para recibir la versión secundaria de la biblioteca del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="97f1e-111">A pointer to a variable to receive the minor version of the offline registry library.</span></span> <span data-ttu-id="97f1e-112">Para la versión inicial de la biblioteca, el valor es 0.</span><span class="sxs-lookup"><span data-stu-id="97f1e-112">For the initial release of the library, the value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97f1e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97f1e-113">Return value</span></span>

<span data-ttu-id="97f1e-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="97f1e-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f1e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97f1e-115">Requirements</span></span>



| <span data-ttu-id="97f1e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="97f1e-116">Requirement</span></span> | <span data-ttu-id="97f1e-117">Value</span><span class="sxs-lookup"><span data-stu-id="97f1e-117">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97f1e-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="97f1e-118">Redistributable</span></span><br/> | <span data-ttu-id="97f1e-119">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="97f1e-119">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="97f1e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97f1e-120">Header</span></span><br/>          | <dl> <span data-ttu-id="97f1e-121"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="97f1e-121"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="97f1e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97f1e-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="97f1e-123"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97f1e-123"><dt>Offreg.dll</dt></span></span> </dl> |



 

 





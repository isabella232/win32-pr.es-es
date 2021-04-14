---
description: Obtiene el nivel de una regla de identificación hash que coincide con el hash especificado.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496487"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="8042b-103">SaferiSearchMatchingHashRules función)</span><span class="sxs-lookup"><span data-stu-id="8042b-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="8042b-104">Obtiene el nivel de una regla de identificación hash que coincide con el hash especificado.</span><span class="sxs-lookup"><span data-stu-id="8042b-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="8042b-105">Esta función no tiene asociada ninguna biblioteca de importación y no está declarada en un encabezado público.</span><span class="sxs-lookup"><span data-stu-id="8042b-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="8042b-106">Debe definir un puntero a función con la firma de esta función, y debe usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="8042b-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="8042b-107">Se recomienda usar la función [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) para evaluar las directivas de restricción de software.</span><span class="sxs-lookup"><span data-stu-id="8042b-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="8042b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8042b-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8042b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8042b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8042b-110">*HashAlgorithm* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8042b-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8042b-111">Identificador del algoritmo utilizado para crear el hash.</span><span class="sxs-lookup"><span data-stu-id="8042b-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="8042b-112">*pHashBytes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8042b-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8042b-113">Puntero a una matriz de bytes que contiene el hash.</span><span class="sxs-lookup"><span data-stu-id="8042b-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="8042b-114">*dwHashSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8042b-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8042b-115">Tamaño, en bytes, de la matriz *pHashBytes* .</span><span class="sxs-lookup"><span data-stu-id="8042b-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="8042b-116">*dwOriginalImageSize* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8042b-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8042b-117">Tamaño, en bytes, de la imagen original a partir de la cual se calculó el hash.</span><span class="sxs-lookup"><span data-stu-id="8042b-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="8042b-118">*pdwFoundLevel* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8042b-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8042b-119">Puntero al identificador de nivel para la regla de identificación hash coincidente.</span><span class="sxs-lookup"><span data-stu-id="8042b-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="8042b-120">*pdwSaferFlags*</span><span class="sxs-lookup"><span data-stu-id="8042b-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8042b-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8042b-121">Reserved.</span></span> <span data-ttu-id="8042b-122">Establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="8042b-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8042b-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8042b-123">Return value</span></span>

<span data-ttu-id="8042b-124">**True** si la función se realiza correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="8042b-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8042b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8042b-125">Requirements</span></span>



| <span data-ttu-id="8042b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8042b-126">Requirement</span></span> | <span data-ttu-id="8042b-127">Value</span><span class="sxs-lookup"><span data-stu-id="8042b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8042b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8042b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8042b-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8042b-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8042b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8042b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8042b-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8042b-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8042b-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8042b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8042b-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8042b-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 

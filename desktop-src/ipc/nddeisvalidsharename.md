---
description: Determina si un nombre de recurso compartido utiliza la sintaxis correcta.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Función NDdeIsValidShareName (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686528"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="1ff7a-103">NDdeIsValidShareName función)</span><span class="sxs-lookup"><span data-stu-id="1ff7a-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="1ff7a-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="1ff7a-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="1ff7a-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="1ff7a-106">Determina si un nombre de recurso compartido utiliza la sintaxis correcta.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff7a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ff7a-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="1ff7a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ff7a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff7a-109">*nombreDeRecursoCompartido* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ff7a-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff7a-110">Nombre del recurso compartido que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-110">The share name to be validated.</span></span> <span data-ttu-id="1ff7a-111">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff7a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ff7a-112">Return value</span></span>

<span data-ttu-id="1ff7a-113">Si el nombre del recurso compartido tiene una sintaxis válida, el valor devuelto es distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="1ff7a-114">Si el nombre del recurso compartido no tiene una sintaxis válida, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff7a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ff7a-115">Remarks</span></span>

<span data-ttu-id="1ff7a-116">[**NDdeShareAdd**](nddeshareadd.md) también llama a esta función cuando crea el recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="1ff7a-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff7a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ff7a-117">Requirements</span></span>



| <span data-ttu-id="1ff7a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ff7a-118">Requirement</span></span> | <span data-ttu-id="1ff7a-119">Value</span><span class="sxs-lookup"><span data-stu-id="1ff7a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff7a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ff7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ff7a-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1ff7a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1ff7a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ff7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ff7a-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ff7a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1ff7a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ff7a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ff7a-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff7a-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ff7a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ff7a-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ff7a-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ff7a-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ff7a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ff7a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ff7a-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ff7a-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="1ff7a-130">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1ff7a-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ff7a-131">**NDdeIsValidShareNameW** (Unicode) y **NDdeIsValidShareNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ff7a-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="1ff7a-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ff7a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff7a-133">Información general de Intercambio dinámico de datos de red</span><span class="sxs-lookup"><span data-stu-id="1ff7a-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="1ff7a-134">Funciones DDE de red</span><span class="sxs-lookup"><span data-stu-id="1ff7a-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="1ff7a-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="1ff7a-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 





---
title: Función RtmCloseEnumerationHandle (RTM. h)
description: RtmCloseEnumerationHandle finaliza una enumeración especificada y libera los recursos asociados.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- RtmCloseEnumerationHandle función RAS
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079517"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="fe47b-104">RtmCloseEnumerationHandle función)</span><span class="sxs-lookup"><span data-stu-id="fe47b-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="fe47b-105">\[Esta API se ha sustituido por la API del [Administrador de tablas de enrutamiento versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fe47b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="fe47b-106">Las aplicaciones deben usar la API del administrador de tabla de enrutamiento versión 2.\]</span><span class="sxs-lookup"><span data-stu-id="fe47b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="fe47b-107">**RtmCloseEnumerationHandle** finaliza una enumeración especificada y libera los recursos asociados.</span><span class="sxs-lookup"><span data-stu-id="fe47b-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe47b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe47b-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="fe47b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe47b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe47b-110">*EnumerationHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fe47b-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe47b-111">Identificador de la enumeración que se va a finalizar.</span><span class="sxs-lookup"><span data-stu-id="fe47b-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="fe47b-112">Obtenga este identificador llamando a [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="fe47b-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe47b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe47b-113">Return value</span></span>

<span data-ttu-id="fe47b-114">Si la función se ejecuta correctamente, el valor devuelto NO es un \_ error.</span><span class="sxs-lookup"><span data-stu-id="fe47b-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="fe47b-115">Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.</span><span class="sxs-lookup"><span data-stu-id="fe47b-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="fe47b-116">Value</span><span class="sxs-lookup"><span data-stu-id="fe47b-116">Value</span></span>                                                                                                       | <span data-ttu-id="fe47b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe47b-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe47b-118"><dt>**ERROR \_ de \_ identificador no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="fe47b-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="fe47b-119">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="fe47b-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="fe47b-120"><dt>**ERROR: \_ no hay \_ recursos del sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fe47b-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="fe47b-121">No hay suficientes recursos para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fe47b-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe47b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe47b-122">Requirements</span></span>



| <span data-ttu-id="fe47b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe47b-123">Requirement</span></span> | <span data-ttu-id="fe47b-124">Value</span><span class="sxs-lookup"><span data-stu-id="fe47b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe47b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe47b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fe47b-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fe47b-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="fe47b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe47b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fe47b-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fe47b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe47b-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fe47b-129">End of server support</span></span><br/>    | <span data-ttu-id="fe47b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fe47b-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="fe47b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe47b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe47b-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe47b-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe47b-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe47b-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe47b-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe47b-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe47b-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe47b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe47b-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe47b-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe47b-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe47b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe47b-138">Referencia de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="fe47b-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="fe47b-139">Funciones de la versión 1 del administrador de tablas de enrutamiento</span><span class="sxs-lookup"><span data-stu-id="fe47b-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="fe47b-140">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="fe47b-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="fe47b-141">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="fe47b-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 






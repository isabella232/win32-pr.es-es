---
title: Función de devolución de llamada PxeProviderInitialize
description: Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Función de devolución de llamada PxeProviderInitialize servicios de implementación de Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705185"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="cc6f0-104">Función de devolución de llamada PxeProviderInitialize</span><span class="sxs-lookup"><span data-stu-id="cc6f0-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="cc6f0-105">Exportación de una biblioteca de vínculos dinámicos (DLL) de proveedor que inicializa el proveedor y lo prepara para recibir solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="cc6f0-106">Los proveedores son necesarios para exportar la función *PxeProviderInitialize* .</span><span class="sxs-lookup"><span data-stu-id="cc6f0-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="cc6f0-107">Todas las devoluciones de llamada al proveedor se deben registrar con una llamada a la función [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante el procesamiento de *PxeProviderInitialize*.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="cc6f0-108">En la devolución de esta función, el proveedor debe inicializarse completamente y estar listo para procesar solicitudes de cliente.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6f0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc6f0-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="cc6f0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc6f0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc6f0-111">*hProvider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc6f0-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6f0-112">Identificador de la instancia del proveedor.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-112">Handle to the provider instance.</span></span> <span data-ttu-id="cc6f0-113">Este identificador debe almacenarse por el proveedor y usarse en cualquier llamada subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="cc6f0-114">Este identificador es válido hasta que se llama a la función de devolución de llamada [*PxeProviderShutdown*](pxeprovidershutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="cc6f0-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="cc6f0-115">*hProviderKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc6f0-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6f0-116">Identificador de una clave del registro en la que se va a almacenar la información de configuración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc6f0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc6f0-117">Return value</span></span>

<span data-ttu-id="cc6f0-118">Si la inicialización del proveedor se realiza correctamente, la devolución de llamada debe devolver el **error \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="cc6f0-119">En caso de error, se debe devolver un código de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="cc6f0-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc6f0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc6f0-120">Requirements</span></span>



| <span data-ttu-id="cc6f0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc6f0-121">Requirement</span></span> | <span data-ttu-id="cc6f0-122">Value</span><span class="sxs-lookup"><span data-stu-id="cc6f0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6f0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc6f0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6f0-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc6f0-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="cc6f0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc6f0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6f0-126">Windows Server 2008, Windows Server 2003 con \[ solo aplicaciones de escritorio de SP2\]</span><span class="sxs-lookup"><span data-stu-id="cc6f0-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc6f0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc6f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc6f0-128">Funciones de servidor de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="cc6f0-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="cc6f0-129">*PxeProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="cc6f0-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 






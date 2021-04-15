---
title: D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
description: Crea un objeto de generador que se puede usar para crear recursos de Direct2D. | D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) (función) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105649365"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><span data-ttu-id="df4b9-105">D2D1CreateFactory <Factory> ( \_ \_ tipo de generador D2D1, Factory \* \* ) (función)</span><span class="sxs-lookup"><span data-stu-id="df4b9-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,Factory\*\*) Function</span></span>

<span data-ttu-id="df4b9-106">Crea un objeto de generador que se puede usar para crear recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="df4b9-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="df4b9-107">Parámetros de plantilla</span><span class="sxs-lookup"><span data-stu-id="df4b9-107">Template Parameters</span></span>



| <span data-ttu-id="df4b9-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="df4b9-108">Parameter</span></span> | <span data-ttu-id="df4b9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="df4b9-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="df4b9-110">*Factory*</span><span class="sxs-lookup"><span data-stu-id="df4b9-110">*Factory*</span></span> | <span data-ttu-id="df4b9-111">Tipo de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="df4b9-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="df4b9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df4b9-112">Parameters</span></span>



| <span data-ttu-id="df4b9-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="df4b9-113">Parameter</span></span>     | <span data-ttu-id="df4b9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="df4b9-114">Description</span></span>                                                                     |
|---------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="df4b9-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="df4b9-115">*factoryType*</span></span> | <span data-ttu-id="df4b9-116">El modelo de subprocesos del generador y los recursos que crea.</span><span class="sxs-lookup"><span data-stu-id="df4b9-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="df4b9-117">*fábrica*</span><span class="sxs-lookup"><span data-stu-id="df4b9-117">*factory*</span></span>     | <span data-ttu-id="df4b9-118">Cuando este método finaliza, contiene la dirección de un puntero al nuevo generador.</span><span class="sxs-lookup"><span data-stu-id="df4b9-118">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="df4b9-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df4b9-119">Return Value</span></span>

<span data-ttu-id="df4b9-120">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="df4b9-120">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df4b9-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="df4b9-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="examples"></a><span data-ttu-id="df4b9-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="df4b9-122">Examples</span></span>

<span data-ttu-id="df4b9-123">En el ejemplo siguiente se crea un generador.</span><span class="sxs-lookup"><span data-stu-id="df4b9-123">The following example creates a factory.</span></span>


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="df4b9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df4b9-124">Requirements</span></span>



| <span data-ttu-id="df4b9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="df4b9-125">Requirement</span></span> | <span data-ttu-id="df4b9-126">Value</span><span class="sxs-lookup"><span data-stu-id="df4b9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4b9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df4b9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df4b9-128">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="df4b9-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="df4b9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df4b9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df4b9-130">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="df4b9-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="df4b9-131">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df4b9-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="df4b9-132">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="df4b9-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="df4b9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df4b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="df4b9-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="df4b9-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="df4b9-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df4b9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="df4b9-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df4b9-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="df4b9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df4b9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df4b9-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df4b9-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 


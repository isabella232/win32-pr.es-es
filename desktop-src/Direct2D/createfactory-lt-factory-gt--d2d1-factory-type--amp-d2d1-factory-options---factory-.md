---
title: D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (función) (D2d1. h)
description: Crea un objeto de generador que se puede usar para crear recursos de Direct2D. | D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (función) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (función) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105660089"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a><span data-ttu-id="77519-105">D2D1CreateFactory <Factory> ( \_ \_ tipo de generador D2D1, D2D1 \_ Factory \_ Options&, Factory \* \* ) function</span><span class="sxs-lookup"><span data-stu-id="77519-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,D2D1\_FACTORY\_OPTIONS&,Factory\*\*) Function</span></span>

<span data-ttu-id="77519-106">Crea un objeto de generador que se puede usar para crear recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="77519-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="77519-107">Parámetros de plantilla</span><span class="sxs-lookup"><span data-stu-id="77519-107">Template Parameters</span></span>



| <span data-ttu-id="77519-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="77519-108">Parameter</span></span> | <span data-ttu-id="77519-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="77519-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="77519-110">*Factory*</span><span class="sxs-lookup"><span data-stu-id="77519-110">*Factory*</span></span> | <span data-ttu-id="77519-111">Tipo de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="77519-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="77519-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77519-112">Parameters</span></span>



| <span data-ttu-id="77519-113">Parámetro</span><span class="sxs-lookup"><span data-stu-id="77519-113">Parameter</span></span>        | <span data-ttu-id="77519-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="77519-114">Description</span></span>                                                                     |
|------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="77519-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="77519-115">*factoryType*</span></span>    | <span data-ttu-id="77519-116">El modelo de subprocesos del generador y los recursos que crea.</span><span class="sxs-lookup"><span data-stu-id="77519-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="77519-117">*factoryOptions*</span><span class="sxs-lookup"><span data-stu-id="77519-117">*factoryOptions*</span></span> | <span data-ttu-id="77519-118">El nivel de detalle proporcionado a la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="77519-118">The level of detail provided to the debugging layer.</span></span>                            |
| <span data-ttu-id="77519-119">*fábrica*</span><span class="sxs-lookup"><span data-stu-id="77519-119">*factory*</span></span>        | <span data-ttu-id="77519-120">Cuando este método finaliza, contiene la dirección de un puntero al nuevo generador.</span><span class="sxs-lookup"><span data-stu-id="77519-120">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="77519-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77519-121">Return Value</span></span>

<span data-ttu-id="77519-122">Si el método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="77519-122">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="77519-123">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77519-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="77519-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77519-124">Requirements</span></span>



| <span data-ttu-id="77519-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="77519-125">Requirement</span></span> | <span data-ttu-id="77519-126">Value</span><span class="sxs-lookup"><span data-stu-id="77519-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77519-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77519-127">Minimum supported client</span></span><br/> | <span data-ttu-id="77519-128">Windows 7, Windows Vista con SP2 y actualización de plataforma para aplicaciones de UWP de aplicaciones de escritorio de Windows Vista \[ \|\]</span><span class="sxs-lookup"><span data-stu-id="77519-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="77519-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77519-129">Minimum supported server</span></span><br/> | <span data-ttu-id="77519-130">Windows Server 2008 R2, Windows Server 2008 con SP2 y la actualización de la plataforma de aplicaciones de escritorio de Windows Server 2008 \[ \| aplicaciones para UWP\]</span><span class="sxs-lookup"><span data-stu-id="77519-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="77519-131">Teléfono mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="77519-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="77519-132">Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]</span><span class="sxs-lookup"><span data-stu-id="77519-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="77519-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="77519-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="77519-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="77519-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="77519-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77519-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="77519-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77519-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="77519-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="77519-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77519-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77519-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 


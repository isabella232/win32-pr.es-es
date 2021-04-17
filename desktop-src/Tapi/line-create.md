---
description: '\_Se envía el mensaje de creación de línea TAPI para informar a la aplicación de la creación de un nuevo dispositivo de línea.'
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Mensaje de LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690414"
---
# <a name="line_create-message"></a><span data-ttu-id="a06dc-103">Mensaje de creación de línea \_</span><span class="sxs-lookup"><span data-stu-id="a06dc-103">LINE\_CREATE message</span></span>

<span data-ttu-id="a06dc-104">Se envía el mensaje de **\_ creación de línea** TAPI para informar a la aplicación de la creación de un nuevo dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="a06dc-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a06dc-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a06dc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a06dc-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a06dc-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a06dc-107">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="a06dc-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="a06dc-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a06dc-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a06dc-109">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="a06dc-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="a06dc-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a06dc-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a06dc-111">*HDeviceID* del dispositivo recién creado.</span><span class="sxs-lookup"><span data-stu-id="a06dc-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="a06dc-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="a06dc-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="a06dc-113">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="a06dc-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="a06dc-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="a06dc-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="a06dc-115">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="a06dc-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a06dc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a06dc-116">Return value</span></span>

<span data-ttu-id="a06dc-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a06dc-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a06dc-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a06dc-118">Remarks</span></span>

<span data-ttu-id="a06dc-119">Las aplicaciones anteriores (que negoció la versión 1,3 de TAPI) se envían a un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que especifica LINEDEVSTATE \_ reinit, que les obliga a apagar el uso de la API y a llamar a [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) de nuevo para obtener el nuevo número de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a06dc-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="a06dc-120">Sin embargo, a diferencia de las versiones anteriores de TAPI, esta versión no requiere que se cierren todas las aplicaciones antes de permitir que las aplicaciones se reinicialicen. la reinicialización puede tener lugar inmediatamente cuando se crea un nuevo dispositivo (el cierre completo sigue siendo necesario cuando se quita un proveedor de servicios del sistema).</span><span class="sxs-lookup"><span data-stu-id="a06dc-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="a06dc-121">Las aplicaciones que admiten la versión 1,4 o posterior de TAPI se envían al mensaje de **\_ creación de línea** .</span><span class="sxs-lookup"><span data-stu-id="a06dc-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="a06dc-122">Esto informa de la existencia del nuevo dispositivo y su nuevo identificador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a06dc-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="a06dc-123">A continuación, la aplicación puede elegir si desea o no intentar trabajar con el nuevo dispositivo en su momento.</span><span class="sxs-lookup"><span data-stu-id="a06dc-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="a06dc-124">Este mensaje se envía a todas las aplicaciones que admiten esta versión o versiones posteriores de la API que han llamado a [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) o [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluidos los que no tienen dispositivos de línea abiertos en este momento.</span><span class="sxs-lookup"><span data-stu-id="a06dc-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="a06dc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a06dc-125">Requirements</span></span>



| <span data-ttu-id="a06dc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a06dc-126">Requirement</span></span> | <span data-ttu-id="a06dc-127">Value</span><span class="sxs-lookup"><span data-stu-id="a06dc-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a06dc-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="a06dc-128">TAPI version</span></span><br/> | <span data-ttu-id="a06dc-129">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="a06dc-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="a06dc-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a06dc-130">Header</span></span><br/>       | <dl> <span data-ttu-id="a06dc-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a06dc-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a06dc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a06dc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a06dc-133">**LÍNEA \_ LINEDEVSTATE**</span><span class="sxs-lookup"><span data-stu-id="a06dc-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="a06dc-134">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="a06dc-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="a06dc-135">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="a06dc-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 





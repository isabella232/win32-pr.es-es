---
description: ITStreamQualityControl expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de flujo.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interfaz ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680450"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="261da-103">Interfaz ITStreamQualityControl</span><span class="sxs-lookup"><span data-stu-id="261da-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="261da-104">\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="261da-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="261da-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="261da-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="261da-106">**ITStreamQualityControl** expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de flujo.</span><span class="sxs-lookup"><span data-stu-id="261da-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="261da-107">Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="261da-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="261da-108">Solo se expone cuando una llamada utiliza estos proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="261da-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="261da-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="261da-109">Members</span></span>

<span data-ttu-id="261da-110">La interfaz **ITStreamQualityControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="261da-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="261da-111">**ITStreamQualityControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="261da-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="261da-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="261da-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="261da-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="261da-113">Methods</span></span>

<span data-ttu-id="261da-114">La interfaz **ITStreamQualityControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="261da-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="261da-115">Método</span><span class="sxs-lookup"><span data-stu-id="261da-115">Method</span></span>                                              | <span data-ttu-id="261da-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="261da-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="261da-117">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="261da-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="261da-118">Obtiene el valor de una [propiedad de calidad de flujo](streamqualityproperty.md)especificada.</span><span class="sxs-lookup"><span data-stu-id="261da-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="261da-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="261da-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="261da-120">Obtiene el intervalo de valores válidos para una [propiedad de calidad de flujo](streamqualityproperty.md)especificada.</span><span class="sxs-lookup"><span data-stu-id="261da-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="261da-121">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="261da-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="261da-122">Establece el valor de una [propiedad de calidad de flujo](streamqualityproperty.md)especificada.</span><span class="sxs-lookup"><span data-stu-id="261da-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="261da-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="261da-123">Requirements</span></span>



| <span data-ttu-id="261da-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="261da-124">Requirement</span></span> | <span data-ttu-id="261da-125">Value</span><span class="sxs-lookup"><span data-stu-id="261da-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="261da-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="261da-126">TAPI version</span></span><br/> | <span data-ttu-id="261da-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="261da-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="261da-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="261da-128">Header</span></span><br/>       | <dl> <span data-ttu-id="261da-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="261da-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="261da-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="261da-130">Library</span></span><br/>      | <dl> <span data-ttu-id="261da-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="261da-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="261da-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="261da-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="261da-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="261da-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 


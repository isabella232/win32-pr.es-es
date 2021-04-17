---
description: La interfaz ITCallQualityControl expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de llamadas.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interfaz ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680209"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="647fd-103">Interfaz ITCallQualityControl</span><span class="sxs-lookup"><span data-stu-id="647fd-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="647fd-104">\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="647fd-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="647fd-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="647fd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="647fd-106">La interfaz **ITCallQualityControl** expone métodos que permiten a una aplicación obtener y establecer parámetros para el control de calidad de llamadas.</span><span class="sxs-lookup"><span data-stu-id="647fd-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="647fd-107">Esta interfaz la implementa [IPCONF MSP](ipconf-msp.md) y el MSP de [H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="647fd-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="647fd-108">Solo se expone cuando una llamada utiliza estos proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="647fd-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="647fd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="647fd-109">Members</span></span>

<span data-ttu-id="647fd-110">La interfaz **ITCallQualityControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="647fd-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="647fd-111">**ITCallQualityControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="647fd-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="647fd-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="647fd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="647fd-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="647fd-113">Methods</span></span>

<span data-ttu-id="647fd-114">La interfaz **ITCallQualityControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="647fd-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="647fd-115">Método</span><span class="sxs-lookup"><span data-stu-id="647fd-115">Method</span></span>                                            | <span data-ttu-id="647fd-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="647fd-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="647fd-117">**Obtener**</span><span class="sxs-lookup"><span data-stu-id="647fd-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="647fd-118">Obtiene el valor de una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="647fd-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="647fd-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="647fd-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="647fd-120">Obtiene el intervalo de valores válidos para una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="647fd-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="647fd-121">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="647fd-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="647fd-122">Establece el valor de una [propiedad de control de calidad de llamada](callqualityproperty.md)determinada.</span><span class="sxs-lookup"><span data-stu-id="647fd-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="647fd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="647fd-123">Requirements</span></span>



| <span data-ttu-id="647fd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="647fd-124">Requirement</span></span> | <span data-ttu-id="647fd-125">Value</span><span class="sxs-lookup"><span data-stu-id="647fd-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="647fd-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="647fd-126">TAPI version</span></span><br/> | <span data-ttu-id="647fd-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="647fd-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="647fd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="647fd-128">Header</span></span><br/>       | <dl> <span data-ttu-id="647fd-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="647fd-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="647fd-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="647fd-130">Library</span></span><br/>      | <dl> <span data-ttu-id="647fd-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="647fd-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="647fd-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="647fd-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="647fd-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="647fd-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 


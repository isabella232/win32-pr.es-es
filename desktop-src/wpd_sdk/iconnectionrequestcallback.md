---
description: Define un método de devolución de llamada único.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Interfaz IConnectionRequestCallback (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003062"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="34847-103">Interfaz IConnectionRequestCallback</span><span class="sxs-lookup"><span data-stu-id="34847-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="34847-104">La interfaz **IConnectionRequestCallback** define un método de devolución de llamada único.</span><span class="sxs-lookup"><span data-stu-id="34847-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="34847-105">Una aplicación de dispositivos portátiles de Windows (WPD) implementa esta interfaz opcional del modelo de objetos componentes (COM) para recibir notificaciones sobre las solicitudes completadas y cancelar las solicitudes pendientes.</span><span class="sxs-lookup"><span data-stu-id="34847-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="34847-106">Las solicitudes se envían mediante los métodos [**IPortableDeviceConnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) y [**IPortableDeviceConnector::D Ulta**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="34847-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="34847-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="34847-107">Members</span></span>

<span data-ttu-id="34847-108">La interfaz **IConnectionRequestCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="34847-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="34847-109">**IConnectionRequestCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="34847-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="34847-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="34847-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="34847-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="34847-111">Methods</span></span>

<span data-ttu-id="34847-112">La interfaz **IConnectionRequestCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="34847-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="34847-113">Método</span><span class="sxs-lookup"><span data-stu-id="34847-113">Method</span></span>                                                      | <span data-ttu-id="34847-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="34847-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="34847-115">**OnComplete (**</span><span class="sxs-lookup"><span data-stu-id="34847-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="34847-116">Notifica a una aplicación que se ha completado una solicitud programada previamente.</span><span class="sxs-lookup"><span data-stu-id="34847-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="34847-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34847-117">Requirements</span></span>



| <span data-ttu-id="34847-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34847-118">Requirement</span></span> | <span data-ttu-id="34847-119">Value</span><span class="sxs-lookup"><span data-stu-id="34847-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34847-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34847-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34847-121">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="34847-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="34847-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34847-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34847-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="34847-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="34847-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34847-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34847-125"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="34847-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="34847-126">IDL</span><span class="sxs-lookup"><span data-stu-id="34847-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34847-127"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34847-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="34847-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="34847-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="34847-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34847-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 


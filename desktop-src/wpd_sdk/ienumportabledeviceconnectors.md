---
description: Admite la enumeración de interfaces de IPortableDeviceConnector, que representan dispositivos MTP/Bluetooth que se emparejaron con el equipo.
ms.assetid: 99aa1e89-5e20-4f6e-82b5-acf63305eba0
title: Interfaz IEnumPortableDeviceConnectors (Devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 7c5340502c7653283e2ea1f2d02e35e7d1222f35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276877"
---
# <a name="ienumportabledeviceconnectors-interface"></a><span data-ttu-id="a4051-103">Interfaz IEnumPortableDeviceConnectors</span><span class="sxs-lookup"><span data-stu-id="a4051-103">IEnumPortableDeviceConnectors interface</span></span>

<span data-ttu-id="a4051-104">La interfaz **IEnumPortableDeviceConnectors** admite la enumeración de interfaces [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) , que representan dispositivos MTP/Bluetooth que se emparejaron con el equipo.</span><span class="sxs-lookup"><span data-stu-id="a4051-104">The **IEnumPortableDeviceConnectors** interface supports the enumeration of [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) interfaces, representing MTP/Bluetooth devices that were paired with the PC.</span></span> <span data-ttu-id="a4051-105">Tenga en cuenta que esto recuperará todos los dispositivos emparejados previamente, incluidos los dispositivos emparejados pero desconectados.</span><span class="sxs-lookup"><span data-stu-id="a4051-105">Note that this will retrieve all previously-paired devices, including devices that are paired but disconnected.</span></span> <span data-ttu-id="a4051-106">Para determinar si un dispositivo sigue conectado, consulte la propiedad **DEVPKEY \_ MTPBTH \_ IsConnected** para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a4051-106">To determine if a device is still connected, query the **DEVPKEY\_MTPBTH\_IsConnected** property for that device.</span></span>

## <a name="members"></a><span data-ttu-id="a4051-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a4051-107">Members</span></span>

<span data-ttu-id="a4051-108">La interfaz **IEnumPortableDeviceConnectors** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4051-108">The **IEnumPortableDeviceConnectors** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a4051-109">**IEnumPortableDeviceConnectors** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a4051-109">**IEnumPortableDeviceConnectors** also has these types of members:</span></span>

-   [<span data-ttu-id="a4051-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4051-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a4051-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a4051-111">Methods</span></span>

<span data-ttu-id="a4051-112">La interfaz **IEnumPortableDeviceConnectors** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a4051-112">The **IEnumPortableDeviceConnectors** interface has these methods.</span></span>



| <span data-ttu-id="a4051-113">Método</span><span class="sxs-lookup"><span data-stu-id="a4051-113">Method</span></span>                                               | <span data-ttu-id="a4051-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4051-114">Description</span></span>                                                                                                                                 |
|:-----------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4051-115">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="a4051-115">**Clone**</span></span>](ienumportabledeviceconnectors-clone.md) | <span data-ttu-id="a4051-116">Crea una copia de la interfaz **IEnumPortableDeviceConnectors** actual.</span><span class="sxs-lookup"><span data-stu-id="a4051-116">Creates a copy of the current **IEnumPortableDeviceConnectors** interface.</span></span><br/>                                                       |
| [<span data-ttu-id="a4051-117">**Next**</span><span class="sxs-lookup"><span data-stu-id="a4051-117">**Next**</span></span>](ienumportabledeviceconnectors-next.md)   | <span data-ttu-id="a4051-118">Recupera los siguientes objetos [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="a4051-118">Retrieves the next one or more [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector) objects in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="a4051-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="a4051-119">**Reset**</span></span>](ienumportabledeviceconnectors-reset.md) | <span data-ttu-id="a4051-120">Restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="a4051-120">Resets the enumeration sequence to the beginning.</span></span><br/>                                                                                |
| [<span data-ttu-id="a4051-121">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="a4051-121">**Skip**</span></span>](ienumportabledeviceconnectors-skip.md)   | <span data-ttu-id="a4051-122">Omite el número especificado de dispositivos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="a4051-122">Skips the specified number of devices in the enumeration sequence.</span></span><br/>                                                               |



 

## <a name="requirements"></a><span data-ttu-id="a4051-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4051-123">Requirements</span></span>



| <span data-ttu-id="a4051-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4051-124">Requirement</span></span> | <span data-ttu-id="a4051-125">Value</span><span class="sxs-lookup"><span data-stu-id="a4051-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4051-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4051-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a4051-127">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="a4051-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="a4051-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a4051-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a4051-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a4051-129">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="a4051-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4051-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4051-131"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4051-131"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="a4051-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a4051-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4051-133"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4051-133"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="a4051-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4051-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4051-135"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4051-135"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 


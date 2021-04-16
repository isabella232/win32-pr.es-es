---
description: 'El controlador de dispositivo usa la interfaz IWpdSerializer para serializar las interfaces IPortableDeviceValues en los búferes de datos sin procesar que se usan para comunicarse con la aplicación. Las aplicaciones no necesitan usar esta interfaz, porque los datos se serializan y deserializan automáticamente al llamar a IPortableDevice:: SendCommand. para obtener esta interfaz, llame a CoCreateInstance y pase el IID \_ IWpdSerializer.'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Interfaz IWpdSerializer (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671278"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="d63f0-103">Interfaz IWpdSerializer</span><span class="sxs-lookup"><span data-stu-id="d63f0-103">IWpdSerializer interface</span></span>

<span data-ttu-id="d63f0-104">El controlador de dispositivo usa la interfaz **IWpdSerializer** para serializar las interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) en los búferes de datos sin procesar que se usan para comunicarse con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d63f0-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="d63f0-105">Las aplicaciones no necesitan usar esta interfaz, porque los datos se serializan y deserializan automáticamente al llamar a [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span><span class="sxs-lookup"><span data-stu-id="d63f0-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="d63f0-106">Para obtener esta interfaz, llame a **CoCreateInstance** y pase el **IID \_ IWpdSerializer**.</span><span class="sxs-lookup"><span data-stu-id="d63f0-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="d63f0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d63f0-107">Members</span></span>

<span data-ttu-id="d63f0-108">La interfaz **IWpdSerializer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d63f0-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d63f0-109">**IWpdSerializer** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d63f0-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="d63f0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d63f0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d63f0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d63f0-111">Methods</span></span>

<span data-ttu-id="d63f0-112">La interfaz **IWpdSerializer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d63f0-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="d63f0-113">Método</span><span class="sxs-lookup"><span data-stu-id="d63f0-113">Method</span></span>                                                                                          | <span data-ttu-id="d63f0-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d63f0-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d63f0-115">**GetBufferFromIPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d63f0-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="d63f0-116">Serializa una interfaz **IPortableDeviceValues** enviada a una matriz de bytes asignada.</span><span class="sxs-lookup"><span data-stu-id="d63f0-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="d63f0-117">**GetIPortableDeviceValuesFromBuffer**</span><span class="sxs-lookup"><span data-stu-id="d63f0-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="d63f0-118">Deserializa una matriz de bytes en una interfaz **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="d63f0-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="d63f0-119">**GetSerializedSize**</span><span class="sxs-lookup"><span data-stu-id="d63f0-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="d63f0-120">Calcula el tamaño del búfer necesario para contener una interfaz **IPortableDeviceValues** serializada.</span><span class="sxs-lookup"><span data-stu-id="d63f0-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="d63f0-121">**WriteIPortableDeviceValuesToBuffer**</span><span class="sxs-lookup"><span data-stu-id="d63f0-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="d63f0-122">Serializa una interfaz **IPortableDeviceValues** en una matriz de bytes asignada por el llamador.</span><span class="sxs-lookup"><span data-stu-id="d63f0-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="d63f0-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d63f0-123">Requirements</span></span>



| <span data-ttu-id="d63f0-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d63f0-124">Requirement</span></span> | <span data-ttu-id="d63f0-125">Value</span><span class="sxs-lookup"><span data-stu-id="d63f0-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63f0-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d63f0-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d63f0-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d63f0-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d63f0-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d63f0-128">Library</span></span><br/> | <dl> <span data-ttu-id="d63f0-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d63f0-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63f0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d63f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63f0-131">**Interfaces de controlador**</span><span class="sxs-lookup"><span data-stu-id="d63f0-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 


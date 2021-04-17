---
description: El \_ tipo de \_ enumeración de transportes de dispositivos WPD especifica la relación de herencia para un servicio. Esta enumeración la usa la \_ propiedad de transporte del dispositivo WPD \_ .
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: Enumeración WPD_DEVICE_TRANSPORTS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708161"
---
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="2ed90-104">\_Enumeración de transportes de dispositivos WPD \_</span><span class="sxs-lookup"><span data-stu-id="2ed90-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="2ed90-105">El tipo de enumeración de [**\_ \_ transportes de dispositivos WPD**](/windows/desktop/wpd_sdk/wpd-device-transports) especifica la relación de herencia para un servicio.</span><span class="sxs-lookup"><span data-stu-id="2ed90-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="2ed90-106">Esta enumeración la usa la propiedad de **\_ \_ transporte del dispositivo WPD** .</span><span class="sxs-lookup"><span data-stu-id="2ed90-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed90-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ed90-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="2ed90-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="2ed90-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2ed90-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**transporte de dispositivo WPD no \_ \_ \_ especificado**</span><span class="sxs-lookup"><span data-stu-id="2ed90-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="2ed90-110">No se especificó el tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="2ed90-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="2ed90-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**\_ \_ Puerto USB de transporte de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2ed90-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="2ed90-112">El dispositivo se conecta a través de USB.</span><span class="sxs-lookup"><span data-stu-id="2ed90-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="2ed90-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**\_IP de \_ transporte del dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2ed90-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="2ed90-114">El dispositivo se conecta a través del Protocolo de Internet (IP).</span><span class="sxs-lookup"><span data-stu-id="2ed90-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="2ed90-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**\_Bluetooth de \_ transporte de dispositivos de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="2ed90-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="2ed90-116">El dispositivo se conecta a través de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="2ed90-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2ed90-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ed90-117">Requirements</span></span>



| <span data-ttu-id="2ed90-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed90-118">Requirement</span></span> | <span data-ttu-id="2ed90-119">Value</span><span class="sxs-lookup"><span data-stu-id="2ed90-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed90-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ed90-120">Header</span></span><br/> | <dl> <span data-ttu-id="2ed90-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ed90-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 


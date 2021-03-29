---
title: Mensajes de WM_DEVICECHANGE y Bluetooth
description: Bluetooth incluye \_ mensajes DEVICECHANGE específicos de WM que permiten a los desarrolladores obtener mensajes cuando los dispositivos Bluetooth se someten a cambios de estado.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995342"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a><span data-ttu-id="05a38-103">Mensajes de DEVICECHANGE de Bluetooth y WM \_</span><span class="sxs-lookup"><span data-stu-id="05a38-103">Bluetooth and WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="05a38-104">Bluetooth incluye mensajes [**\_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) específicos de WM que permiten a los desarrolladores obtener mensajes cuando los dispositivos Bluetooth se someten a cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="05a38-104">Bluetooth includes specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages that enable developers to obtain messages when Bluetooth devices undergo status changes.</span></span> <span data-ttu-id="05a38-105">En este tema se describe cómo recibir mensajes de **WM \_ DEVICECHANGE** específicos de Bluetooth y se enumeran los mensajes específicos de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="05a38-105">This topic describes how to receive Bluetooth-specific **WM\_DEVICECHANGE** messages and lists Bluetooth-specific messages.</span></span>

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a><span data-ttu-id="05a38-106">Recepción de mensajes DEVICECHANGE de WM específicos de Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="05a38-106">Receiving Bluetooth-specific WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="05a38-107">Para recibir mensajes de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , primero se debe abrir un identificador para la radio local.</span><span class="sxs-lookup"><span data-stu-id="05a38-107">To receive [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages, a handle to the local radio must first be opened.</span></span> <span data-ttu-id="05a38-108">Para ello, use uno de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="05a38-108">To do this, use one of the following methods:</span></span>

-   <span data-ttu-id="05a38-109">Use la función [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) con los siguientes parámetros: ( \_ \_ interfaz de dispositivo GUID BTHPORT \_ ,..., \_ DIGCF \| present DIGCF \_ DEVICEINTERFACE) y, a continuación, use las funciones [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)y [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .</span><span class="sxs-lookup"><span data-stu-id="05a38-109">Use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function with the following parameters: (GUID\_BTHPORT\_DEVICE\_INTERFACE, …, DIGCF\_PRESENT \| DIGCF\_DEVICEINTERFACE), then use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), and the [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) functions.</span></span>
-   <span data-ttu-id="05a38-110">Use las funciones [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)y [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .</span><span class="sxs-lookup"><span data-stu-id="05a38-110">Use the [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio), and [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) functions.</span></span>

<span data-ttu-id="05a38-111">Cuando se abra el controlador de radio Bluetooth, llame a la función [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) y regístrese para recibir notificaciones en el identificador mediante **DBT \_ DEVTYP \_ Handle** como DeviceType.</span><span class="sxs-lookup"><span data-stu-id="05a38-111">When the Bluetooth radio handle is opened, call the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function and register for notifications on the handle using **DBT\_DEVTYP\_HANDLE** as the devicetype.</span></span> <span data-ttu-id="05a38-112">Cuando se registra, se envían los siguientes GUID y el miembro de datos [**\_ \_ Handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_** de dev es el búfer asociado.</span><span class="sxs-lookup"><span data-stu-id="05a38-112">When registered, the following GUIDs are sent, and the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch\_data** member is the associated buffer.</span></span>

## <a name="bluetooth-specific-messages"></a><span data-ttu-id="05a38-113">Mensajes específicos de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="05a38-113">Bluetooth-specific Messages</span></span>

<span data-ttu-id="05a38-114">En la tabla siguiente se enumeran los mensajes de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) específicos de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="05a38-114">The following table lists Bluetooth-specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages.</span></span>

| <span data-ttu-id="05a38-115">GUID</span><span class="sxs-lookup"><span data-stu-id="05a38-115">GUID</span></span>                                   | <span data-ttu-id="05a38-116">BUFFER</span><span class="sxs-lookup"><span data-stu-id="05a38-116">BUFFER</span></span>                                                  | <span data-ttu-id="05a38-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="05a38-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a38-118">\_ \_ evento HCI de Bluetooth de GUID \_</span><span class="sxs-lookup"><span data-stu-id="05a38-118">GUID\_BLUETOOTH\_HCI\_EVENT</span></span>            | [<span data-ttu-id="05a38-119">**BTH \_ \_ información de evento de HCI \_**</span><span class="sxs-lookup"><span data-stu-id="05a38-119">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | <span data-ttu-id="05a38-120">Este mensaje se envía cuando un dispositivo Bluetooth remoto se conecta o se desconecta en el nivel de ACL.</span><span class="sxs-lookup"><span data-stu-id="05a38-120">This message is sent when a remote Bluetooth device connects or disconnects at the ACL level.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="05a38-121">\_ \_ Evento L2CAP de Bluetooth de GUID \_</span><span class="sxs-lookup"><span data-stu-id="05a38-121">GUID\_BLUETOOTH\_L2CAP\_EVENT</span></span>          | [<span data-ttu-id="05a38-122">**BTH \_ \_ información de evento de L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="05a38-122">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | <span data-ttu-id="05a38-123">Este mensaje se envía cuando se ha establecido o finalizado un canal L2CAP entre la radio local y un dispositivo Bluetooth remoto.</span><span class="sxs-lookup"><span data-stu-id="05a38-123">This message is sent when an L2CAP channel between the local radio and a remote Bluetooth device has been established or terminated.</span></span> <span data-ttu-id="05a38-124">En el caso de los canales L2CAP que son multiplexores, como RFCOMM, este mensaje solo se envía cuando se establece el canal subyacente, no cuando se establece o finaliza cada canal multiplexado, como un canal RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="05a38-124">For L2CAP channels that are multiplexers, such as RFCOMM, this message is only sent when the underlying channel is established, not when each multiplexed channel, such as an RFCOMM channel, is established or terminated.</span></span> |
| <span data-ttu-id="05a38-125">\_solicitud de \_ PIN de Bluetooth de GUID \_</span><span class="sxs-lookup"><span data-stu-id="05a38-125">GUID\_BLUETOOTH\_PIN\_REQUEST</span></span>          | <span data-ttu-id="05a38-126">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="05a38-126">Not applicable.</span></span>                                         | <span data-ttu-id="05a38-127">La aplicación debe pasar por alto este mensaje.</span><span class="sxs-lookup"><span data-stu-id="05a38-127">This message should be ignored by the application.</span></span> <span data-ttu-id="05a38-128">Si la aplicación debe recibir solicitudes de PIN, se debe usar la función [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="05a38-128">If the application must receive PIN requests, the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function should be used.</span></span>                                                                                                                                                   |
| <span data-ttu-id="05a38-129">\_radio Bluetooth \_ de GUID \_ en el \_ intervalo</span><span class="sxs-lookup"><span data-stu-id="05a38-129">GUID\_BLUETOOTH\_RADIO\_IN\_RANGE</span></span>      | [<span data-ttu-id="05a38-130">**\_radio BTH \_ en el \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="05a38-130">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | <span data-ttu-id="05a38-131">Este mensaje se envía cuando cambia cualquiera de los siguientes atributos de un dispositivo Bluetooth remoto: se ha detectado el dispositivo, la clase de dispositivo, el nombre, el estado conectado o el estado recordado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05a38-131">This message is sent when any of the following attributes of a remote Bluetooth device has changed: the device has been discovered, the class of device, name, connected state, or device remembered state.</span></span> <span data-ttu-id="05a38-132">También se envía este mensaje cuando se establecen o borran estos atributos.</span><span class="sxs-lookup"><span data-stu-id="05a38-132">This message is also sent when these attributes are set or cleared.</span></span>                                                                                  |
| <span data-ttu-id="05a38-133">\_radio Bluetooth \_ \_ de GUID fuera \_ del \_ intervalo</span><span class="sxs-lookup"><span data-stu-id="05a38-133">GUID\_BLUETOOTH\_RADIO\_OUT\_OF\_RANGE</span></span> | [<span data-ttu-id="05a38-134">**\_dirección Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="05a38-134">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | <span data-ttu-id="05a38-135">Este mensaje se envía cuando no se ha encontrado un dispositivo detectado anteriormente después de la finalización de la última consulta.</span><span class="sxs-lookup"><span data-stu-id="05a38-135">This message is sent when a previously discovered device has not been found after the completion of the last inquiry.</span></span> <span data-ttu-id="05a38-136">Este mensaje no se enviará para dispositivos recordados.</span><span class="sxs-lookup"><span data-stu-id="05a38-136">This message will not be sent for remembered devices.</span></span> <span data-ttu-id="05a38-137">La estructura de **\_ direcciones BTH** es la dirección del dispositivo que no se encontró.</span><span class="sxs-lookup"><span data-stu-id="05a38-137">The **BTH\_ADDRESS** structure is the address of the device that was not found.</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="05a38-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05a38-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05a38-139">**BluetoothFindFirstRadio**</span><span class="sxs-lookup"><span data-stu-id="05a38-139">**BluetoothFindFirstRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[<span data-ttu-id="05a38-140">**BluetoothFindNextRadio**</span><span class="sxs-lookup"><span data-stu-id="05a38-140">**BluetoothFindNextRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[<span data-ttu-id="05a38-141">**BluetoothFindRadioClose**</span><span class="sxs-lookup"><span data-stu-id="05a38-141">**BluetoothFindRadioClose**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[<span data-ttu-id="05a38-142">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="05a38-142">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[<span data-ttu-id="05a38-143">SetupDiDestroyDeviceInfoList</span><span class="sxs-lookup"><span data-stu-id="05a38-143">SetupDiDestroyDeviceInfoList</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[<span data-ttu-id="05a38-144">SetupDiEnumDeviceInterfaces</span><span class="sxs-lookup"><span data-stu-id="05a38-144">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="05a38-145">SetupDiGetClassDevs</span><span class="sxs-lookup"><span data-stu-id="05a38-145">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="05a38-146">**\_dirección Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="05a38-146">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[<span data-ttu-id="05a38-147">**BTH \_ \_ información de evento de HCI \_**</span><span class="sxs-lookup"><span data-stu-id="05a38-147">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[<span data-ttu-id="05a38-148">**BTH \_ \_ información de evento de L2CAP \_**</span><span class="sxs-lookup"><span data-stu-id="05a38-148">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[<span data-ttu-id="05a38-149">**\_radio BTH \_ en el \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="05a38-149">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[<span data-ttu-id="05a38-150">**\_controlador de difusión de dev \_**</span><span class="sxs-lookup"><span data-stu-id="05a38-150">**DEV\_BROADCAST\_HANDLE**</span></span>](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[<span data-ttu-id="05a38-151">**DEVICECHANGE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="05a38-151">**WM\_DEVICECHANGE**</span></span>](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 
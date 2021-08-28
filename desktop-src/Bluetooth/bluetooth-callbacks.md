---
title: Bluetooth Callbacks
description: Las Bluetooth de devolución de llamada de esta sección se usan en combinación con funciones que hacen posible administrar Bluetooth dispositivos y servicios.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad822a0c7af4b0bbc5d649919bda638776014dfe7e8195ed1f45bb99032c6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588365"
---
# <a name="bluetooth-callbacks"></a>Bluetooth Callbacks

Las Bluetooth de devolución de llamada de esta sección se usan en combinación con funciones que hacen posible administrar Bluetooth dispositivos y servicios.

Bluetooth también se admite mediante la interfaz de programación Windows Sockets. Para obtener más información sobre la programación Bluetooth mediante la interfaz Windows Sockets, vea Compatibilidad Windows [sockets](windows-sockets-support-for-bluetooth.md)de Bluetooth .



| Sección                                                                                      | Content                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE \_ AUTENTICACIÓN PFN**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Se usa junto con la [**función BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)                                                  |
| [**DEVOLUCIÓN DE \_ LLAMADA \_ DE AUTENTICACIÓN PFN, \_ POR EJEMPLO**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Se usa junto con la [**función BluetoothRegisterForAuthenticationEx.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)                                              |
| [**DEVOLUCIÓN DE \_ LLAMADA DE ATRIBUTOS DE \_ \_ ENUMERACIÓN DE BLUETOOTH PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Se llama una vez por cada atributo encontrado en el *parámetro pSDPStream* que se pasa a la llamada de función [**BluetoothSdpEnumAttributes.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) |
| [**DEVOLUCIÓN DE LLAMADA DE DISPOSITIVO PFN \_ \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Se usa en asociación con la selección Bluetooth dispositivos.                                                                                                                    |



 

 

 





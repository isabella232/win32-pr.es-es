---
title: Bluetooth Callbacks
description: Las Bluetooth de devolución de llamada de esta sección se usan en combinación con funciones que hacen posible administrar Bluetooth dispositivos y servicios.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127261895"
---
# <a name="bluetooth-callbacks"></a>Bluetooth Callbacks

Las Bluetooth de devolución de llamada de esta sección se usan en combinación con funciones que hacen posible administrar Bluetooth dispositivos y servicios.

Bluetooth también se admite mediante la interfaz de programación Windows Sockets. Para obtener más información sobre la programación Bluetooth mediante la interfaz Windows Sockets, vea Compatibilidad Windows [sockets](windows-sockets-support-for-bluetooth.md)de Bluetooth .



| Sección                                                                                      | Contenido                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DEVOLUCIÓN DE LLAMADA \_ DE \_ AUTENTICACIÓN PFN**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Se usa junto con la [**función BluetoothRegisterForAuthentication.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)                                                  |
| [**DEVOLUCIÓN DE LLAMADA \_ \_ DE AUTENTICACIÓN \_ PFN, POR EJEMPLO**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Se usa junto con la [**función BluetoothRegisterForAuthenticationEx.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)                                              |
| [**DEVOLUCIÓN DE LLAMADA \_ DE ATRIBUTOS DE ENUMERACIÓN BLUETOOTH \_ \_ \_ PFN**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Se le llama una vez por cada atributo encontrado en el *parámetro pSDPStream* que se pasa a la llamada de función [**BluetoothSdpEnumAttributes.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) |
| [**DEVOLUCIÓN DE LLAMADA \_ DE DISPOSITIVO PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Se usa en asociación con la selección Bluetooth dispositivos.                                                                                                                    |



 

 

 





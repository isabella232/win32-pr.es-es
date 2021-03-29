---
title: Devoluciones de llamada Bluetooth
description: Las funciones de devolución de llamada de Bluetooth en esta sección se usan en combinación con funciones que permiten administrar dispositivos y servicios Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773650"
---
# <a name="bluetooth-callbacks"></a>Devoluciones de llamada Bluetooth

Las funciones de devolución de llamada de Bluetooth en esta sección se usan en combinación con funciones que permiten administrar dispositivos y servicios Bluetooth.

Bluetooth también es compatible con la interfaz de programación de Windows Sockets. Para obtener más información acerca de la programación de Bluetooth mediante la interfaz de Windows Sockets, consulte [compatibilidad de Windows Sockets con Bluetooth](windows-sockets-support-for-bluetooth.md).



| Sección                                                                                      | Contenido                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**devolución de llamada de \_ autenticación pfn \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Se usa junto con la función [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                  |
| [**\_devolución de llamada de autenticación pfn \_ \_ ex**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Se usa junto con la función [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .                                              |
| [**PFN \_ \_ devolución de \_ llamada de atributos de enumeración Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Se le llama una vez para cada atributo que se encuentra en el parámetro *pSDPStream* que se pasa a la llamada a la función [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) . |
| [**devolución de llamada de \_ dispositivo pfn \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Se usa en asociación con la selección de dispositivos Bluetooth.                                                                                                                    |



 

 

 





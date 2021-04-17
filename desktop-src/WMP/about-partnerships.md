---
title: Acerca de las asociaciones
description: Acerca de las asociaciones
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, asociaciones
- Modelo de objetos de Windows Media Player, asociaciones
- modelo de objetos, asociaciones
- Control ActiveX de Windows Media Player, asociaciones
- Control ActiveX, asociaciones
- Control ActiveX móvil de Windows Media Player, asociaciones
- Windows Media Player Mobile, asociaciones
- sincronizar dispositivos, asociaciones
- sincronización de dispositivos, asociaciones
- asociaciones entre dispositivos y Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487283"
---
# <a name="about-partnerships"></a>Acerca de las asociaciones

Una asociación es una relación especial entre un dispositivo portátil y un Media Player de Windows. Los usuarios pueden establecer una asociación para un dispositivo determinado mediante el uso de la interfaz de usuario de Windows Media Player. Puede administrar mediante programación las asociaciones mediante [IWMPSyncDevice:: createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) y [IWMPSyncDevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). El método **createPartnership** inicia un proceso asincrónico que finaliza cuando se recibe el evento **CreatePartnershipComplete** a través de la interfaz **IWMPEvents2** .

Windows Media Player 10 o versiones posteriores admiten la creación de asociaciones con hasta 16 dispositivos. Cada asociación tiene un índice de asociación asociado. Puede recuperar el índice de Asociación para un dispositivo determinado mediante una llamada a [IWMPSyncDevice:: get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Los índices de asociación se numeran de 1 a 16. Cuando un dispositivo determinado no tiene una asociación con Windows Media Player, **getPartnershipIndex** devuelve cero para el índice.

Puede recuperar el estado de Asociación de un dispositivo determinado llamando a [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) y, a continuación, inspeccionando el valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. Windows Media Player permite una asociación con una biblioteca de un usuario en un equipo para cada dispositivo. Esto significa que la creación de una nueva asociación destruye cualquier asociación existente que el dispositivo actual pueda tener con otro equipo. Para saber cuándo cambia el estado de un dispositivo, puede recibir el evento **DeviceStatusChange** .

Windows Media Player no puede crear una asociación con un dispositivo que tenga el estado **wmpdsManualDevice**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**Interfaz IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 





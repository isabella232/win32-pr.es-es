---
title: Acerca de las asociaciones
description: Acerca de las asociaciones
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Reproductor de Windows Media,partnerships
- Reproductor de Windows Media modelo de objetos, asociaciones
- modelo de objetos, asociaciones
- Reproductor de Windows Media ActiveX control, asociaciones
- ActiveX control, asociaciones
- Reproductor de Windows Media Control de ActiveX móviles, asociaciones
- Reproductor de Windows Media Móvil, asociaciones
- sincronizar dispositivos, asociaciones
- sincronización de dispositivos, asociaciones
- asociaciones entre dispositivos y Reproductor de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264844"
---
# <a name="about-partnerships"></a>Acerca de las asociaciones

Una asociación es una relación especial entre un dispositivo portátil y Reproductor de Windows Media. Los usuarios pueden establecer una asociación para un dispositivo determinado mediante la interfaz Reproductor de Windows Media usuario. Puede administrar asociaciones mediante programación mediante [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). El **método createPartnership** inicia un proceso asincrónico que finaliza cuando se recibe el evento **CreatePartnershipComplete** a través de la **interfaz IWMPEvents2.**

Reproductor de Windows Media 10 o posterior admite la creación de asociaciones con hasta 16 dispositivos. Cada asociación tiene un índice de asociación asociado. Puede recuperar el índice de asociación para un dispositivo determinado llamando a [IWMPSyncDevice::get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Los índices de asociación se numeran de 1 a 16. Cuando un dispositivo determinado no tiene una asociación con Reproductor de Windows Media, **getPartnershipIndex** devuelve cero para el índice.

Puede recuperar el estado de asociación de un dispositivo determinado llamando a [IWMPSyncDevice::get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) y, a continuación, inspeccionando el [valor WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. Reproductor de Windows Media permite una asociación con la biblioteca de un usuario en un equipo para cada dispositivo. Esto significa que la creación de una nueva asociación destruye cualquier asociación existente que el dispositivo actual pueda tener con otro equipo. Para saber cuándo cambia el estado de un dispositivo, puede recibir el **evento DeviceStatusChange.**

Reproductor de Windows Media puede crear una asociación con un dispositivo que tenga el estado **wmpdsManualDevice**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Trabajar con dispositivos portátiles**](working-with-portable-devices.md)
</dt> </dl>

 

 





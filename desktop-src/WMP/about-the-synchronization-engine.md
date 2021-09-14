---
title: Acerca del motor de sincronización
description: Acerca del motor de sincronización
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Reproductor de Windows Media,motor de sincronización
- Reproductor de Windows Media de objetos, motor de sincronización
- modelo de objetos, motor de sincronización
- Reproductor de Windows Media ActiveX control,motor de sincronización
- ActiveX control,motor de sincronización
- Reproductor de Windows Media Control de ActiveX móvil, motor de sincronización
- Reproductor de Windows Media Móvil, motor de sincronización
- sincronizar dispositivos, motor de sincronización
- sincronización de dispositivos, motor de sincronización
- motor de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073289"
---
# <a name="about-the-synchronization-engine"></a>Acerca del motor de sincronización

El motor de sincronización es el componente de Reproductor de Windows Media que administra la copia de contenido multimedia digital en dispositivos portátiles. Reproductor de Windows Media admite una única instancia del motor de sincronización para cada dispositivo. Debe usar una instancia remota del control Reproductor de Windows Media para realizar tareas de sincronización mediante programación. De hecho, el programa comparte las instancias del motor de sincronización con Reproductor de Windows Media y todos los demás programas que usan las interfaces del reproductor para la sincronización de dispositivos.

Puede usar [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) para controlar cuándo el motor de sincronización realiza su trabajo. En la mayoría de los casos, no debe usar estos métodos. En su lugar, debe permitir que el motor de sincronización programe su trabajo automáticamente. Los **métodos** start **y stop** existen para que pueda usarlos si el programa está diseñado para reemplazar la interfaz Reproductor de Windows Media usuario. En este caso, es posible que desee proporcionar un botón iniciar o detener similar al que proporciona Reproductor de Windows Media en la **pestaña Dispositivos.**

Puede supervisar el progreso de sincronización de un dispositivo sondear [IWMPSyncDevice::get \_ progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Este método recupera un valor de progreso para todo el proceso de sincronización con un dispositivo determinado. El valor recuperado es un número que representa el porcentaje de sincronización completada. Hay dos eventos que puede recibir relacionados con la sincronización. El **evento DeviceSyncError** le notifica cuándo se produce un problema. El **evento DeviceSyncStateChange** le avisa cuando el motor de sincronización ha cambiado el estado del dispositivo actual.

Puede limitar la cantidad de almacenamiento de dispositivo que Reproductor de Windows Media usa para la sincronización llamando a [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) con el **atributo PercentSpaceReserved.** El uso de esta interfaz Reproductor de Windows Media 11.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 (interfaz)**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Mostrar el progreso de la sincronización**](showing-synchronization-progress.md)
</dt> </dl>

 

 





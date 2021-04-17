---
title: Acerca del motor de sincronización
description: Acerca del motor de sincronización
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, motor de sincronización
- Modelo de objetos de Windows Media Player, motor de sincronización
- modelo de objetos, motor de sincronización
- Control ActiveX de Windows Media Player, motor de sincronización
- Control ActiveX, motor de sincronización
- Control ActiveX móvil de Windows Media Player, motor de sincronización
- Windows Media Player Mobile, motor de sincronización
- sincronizar dispositivos, motor de sincronización
- sincronización de dispositivos, motor de sincronización
- motor de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420291"
---
# <a name="about-the-synchronization-engine"></a>Acerca del motor de sincronización

El motor de sincronización es el componente de Windows Media Player que administra la copia de contenido multimedia digital en dispositivos portátiles. Windows Media Player admite una única instancia del motor de sincronización para cada dispositivo. Debe utilizar una instancia remota del control Media Player de Windows para realizar las tareas de sincronización mediante programación. En efecto, el programa comparte las instancias del motor de sincronización con Windows Media Player y todos los demás programas que usan las interfaces del reproductor para la sincronización de dispositivos.

Puede usar [IWMPSyncDevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) y [IWMPSyncDevice:: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) para controlar el momento en que el motor de sincronización realiza su trabajo. En la mayoría de los casos, no debe utilizar estos métodos. En su lugar, debe permitir que el motor de sincronización Programe su trabajo automáticamente. Los métodos **Start** y **Stop** existen para que pueda usarlos si el programa está diseñado para reemplazar la interfaz de usuario de Windows Media Player. En este caso, es posible que desee proporcionar un botón Iniciar/detener similar al que proporciona Windows Media Player en la pestaña **dispositivos** .

Puede supervisar el progreso de sincronización de un dispositivo mediante el sondeo de [IWMPSyncDevice:: get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Este método recupera un valor de progreso para todo el proceso de sincronización con un dispositivo determinado. El valor recuperado es un número que representa el porcentaje de sincronización completada. Hay dos eventos que se pueden recibir y que están relacionados con la sincronización. El evento **DeviceSyncError** le notifica cuando se produce un problema. El evento **DeviceSyncStateChange** le alerta cuando el motor de sincronización ha cambiado el estado del dispositivo actual.

Puede limitar la cantidad de almacenamiento de dispositivo que usa Windows Media Player para la sincronización mediante una llamada a [IWMPSyncDevice2:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) con el atributo **PercentSpaceReserved** . El uso de esta interfaz requiere Windows Media Player 11.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca de la sincronización de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**Interfaz IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Mostrando el progreso de la sincronización**](showing-synchronization-progress.md)
</dt> </dl>

 

 





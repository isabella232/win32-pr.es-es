---
description: Las constantes DEVICE \_ STATE XXX indican el estado actual de un dispositivo de punto de conexión de \_ audio.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: DEVICE_STATE_XXX constantes (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165038"
---
# <a name="device_state_xxx-constants"></a>Constantes \_ XXX de DEVICE STATE \_

Las constantes DEVICE \_ STATE XXX indican el estado actual de un dispositivo de punto de conexión de \_ audio.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**DISPOSITIVO \_ ESTADO \_ ACTIVO**</dt> <dt>0x00000001</dt> </dl>             | El dispositivo de punto de conexión de audio está activo. Es decir, el adaptador de audio que se conecta al dispositivo del punto de conexión está presente y habilitado. Además, si el dispositivo del punto de conexión se conecta a un conector del adaptador, el dispositivo del punto de conexión está conectado.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**DISPOSITIVO \_ ESTADO \_ DESHABILITADO**</dt> <dt>0x00000002</dt> </dl>       | El dispositivo de punto de conexión de audio está deshabilitado. El usuario ha deshabilitado el dispositivo en el panel de control multimedia Windows, Mmsys.cpl. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**DISPOSITIVO \_ State \_ NOTPRESENT**</dt> <dt>0x00000004</dt> </dl> | El dispositivo de punto de conexión de audio no está presente porque el adaptador de audio que se conecta al dispositivo del punto de conexión se ha quitado del sistema o el usuario ha deshabilitado el dispositivo adaptador en Administrador de dispositivos.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**DISPOSITIVO \_ ESTADO \_ DE 0X00000008**</dt> <dt></dt> </dl>    | El dispositivo de punto de conexión de audio está desconectado. El adaptador de audio que contiene el conector para el dispositivo del punto de conexión está presente y habilitado, pero el dispositivo del punto de conexión no está conectado al conector. Solo un dispositivo con detección de presencia de conector puede estar en este estado. Para obtener más información sobre la detección de presencia de conector, vea [Dispositivos de punto de conexión de audio.](audio-endpoint-devices.md)<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**DISPOSITIVO \_ STATEMASK \_ ALL**</dt> <dt>0x0000000F</dt> </dl>          | Incluye dispositivos de punto de conexión de audio en todos los estados activos, deshabilitados, no presentes y desconectados.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Observaciones

Los [**métodos IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)e [**IMMNotificationClient::OnDeviceStateChanged usan**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) las constantes DEVICE \_ STATE \_ XXX. Estos métodos permiten a los clientes obtener información sobre los dispositivos de punto de conexión que se encuentran en cualquiera de los estados representados por las constantes DEVICE \_ STATE \_ XXX.

Sin embargo, un cliente puede abrir una secuencia (por ejemplo, obteniendo una interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para el dispositivo) solo en un dispositivo que se encuentra en el estado DEVICE \_ STATE \_ ACTIVE.

En Windows panel de control multimedia, Mmsys.cpl, se muestran los dispositivos de punto de conexión de audio en el sistema. Deshabilitar un dispositivo en Mmsys.cpl oculta el dispositivo de los mecanismos de detección de dispositivos en las API de audio de nivel superior, pero no invalida los objetos de secuencia de los que un cliente podría haber creado instancias antes de deshabilitar el dispositivo. Por ejemplo, si una secuencia se reproduce en el dispositivo cuando el usuario la deshabilita en Mmsys.cpl, la secuencia continúa reproduciendo sin interrupciones.

Por el contrario, deshabilitar un dispositivo en Administrador de dispositivos elimina eficazmente el dispositivo del sistema.

Para usar Mmsys.cpl para ver los dispositivos de representación, abra una ventana del símbolo del sistema y escriba el siguiente comando:

**control mmsys.cpl,,0**

Para ver los dispositivos de captura, escriba el siguiente comando:

**control mmsys.cpl,,1**

Como alternativa, puede ver los dispositivos de representación o los dispositivos de captura en Mmsys.cpl haciendo clic con el botón derecho  en el icono del altavoz en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y seleccionando Dispositivos de reproducción o Dispositivos de **grabación.**

Mmsys.cpl muestra siempre los dispositivos de punto de conexión que se encuentran en el estado ESTADO \_ \_ ACTIVO DEL DISPOSITIVO. Además, se puede configurar para mostrar dispositivos deshabilitados y desconectados.

Para ver los dispositivos de punto de conexión que se encuentran en los estados DEVICE STATE DISABLED y DEVICE STATE NOTPRESENT, haga clic con el botón derecho en la ventana Mmsys.cpl y seleccione la opción Mostrar dispositivos \_ \_ \_ \_ deshabilitados. 

Para ver los dispositivos de punto de conexión que están en estado DEVICE STATE UNPLUGGED, haga clic con el botón derecho en la ventana Mmsys.cpl y seleccione la opción Mostrar \_ \_ **dispositivos** desconectados.

Para ver solo los dispositivos de punto de conexión que están en estado ACTIVO ESTADO DE DISPOSITIVO, anule la selección de las opciones Mostrar dispositivos deshabilitados y \_ \_ Mostrar **dispositivos** desconectados. 

Para habilitar o deshabilitar un dispositivo de  punto de conexión en Mmsys.cpl, haga clic en Reproducción o **Grabación,** en función de si el dispositivo es un dispositivo de reproducción o grabación. A continuación, seleccione el dispositivo y haga clic **en Propiedades.** En la **ventana Propiedades,** junto a **Uso del** dispositivo, seleccione Usar este dispositivo **(habilitar)** o No usar este dispositivo **(deshabilitar).**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IMMDevice::GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**IMMDeviceEnumerator (Interfaz)**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 





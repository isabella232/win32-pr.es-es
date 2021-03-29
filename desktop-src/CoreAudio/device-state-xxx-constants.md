---
description: Las \_ constantes de estado del dispositivo \_ XXX indican el estado actual de un dispositivo de punto de conexión de audio.
ms.assetid: d03f2fbc-313a-42cf-902a-fd9f6dce2a35
title: Constantes de DEVICE_STATE_XXX (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65fc09a547ad702d27e96e968915f9d70e3313e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806968"
---
# <a name="device_state_xxx-constants"></a>Constantes de estado de dispositivo \_ \_ XXX

Las \_ constantes de estado del dispositivo \_ XXX indican el estado actual de un dispositivo de punto de conexión de audio.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DEVICE_STATE_ACTIVE"></span><span id="device_state_active"></span><dl> <dt>**Dispositivo \_ de STATE \_ activo**</dt> <dt>0x00000001</dt> </dl>             | El dispositivo de punto de conexión de audio está activo. Es decir, el adaptador de audio que se conecta al dispositivo de extremo está presente y habilitado. Además, si el dispositivo de extremo se conecta a un conector en el adaptador, el dispositivo de extremo está conectado.<br/>                                                                                                                            |
| <span id="DEVICE_STATE_DISABLED"></span><span id="device_state_disabled"></span><dl> <dt>**Dispositivo \_ de ESTADO \_ deshabilitado**</dt> <dt>0x00000002</dt> </dl>       | El dispositivo de punto de conexión de audio está deshabilitado. El usuario ha deshabilitado el dispositivo en el panel de control multimedia de Windows Mmsys.cpl. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                                                        |
| <span id="DEVICE_STATE_NOTPRESENT"></span><span id="device_state_notpresent"></span><dl> <dt>**Dispositivo \_ de ESTADO \_ NOTPRESENT**</dt> <dt>0x00000004</dt> </dl> | El dispositivo de extremo de audio no está presente porque el adaptador de audio que se conecta al dispositivo de extremo se ha quitado del sistema o el usuario ha deshabilitado el dispositivo adaptador en Administrador de dispositivos.<br/>                                                                                                                                                              |
| <span id="DEVICE_STATE_UNPLUGGED"></span><span id="device_state_unplugged"></span><dl> <dt>**Dispositivo \_ de Estado no \_ conectado**</dt> <dt>0x00000008</dt> </dl>    | El dispositivo de punto de conexión de audio está desconectado. El adaptador de audio que contiene el conector para el dispositivo de extremo está presente y habilitado, pero el dispositivo de punto de conexión no está conectado al conector. Solo un dispositivo con detección de la presencia de conector puede estar en este estado. Para obtener más información sobre la detección de la presencia de tomas, consulte [dispositivos de punto de conexión de audio](audio-endpoint-devices.md).<br/> |
| <span id="DEVICE_STATEMASK_ALL"></span><span id="device_statemask_all"></span><dl> <dt>**Dispositivo \_ de STATEMASK \_ todos los**</dt> <dt>0x0000000F</dt> </dl>          | Incluye dispositivos de punto de conexión de audio en todos los Estados activo, deshabilitado, no presente y desconectado.<br/>                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Observaciones

Los métodos [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints), [**IMMDevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)y [**IMMNotificationClient:: OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged) usan las constantes de \_ Estado de dispositivo \_ xxx. Estos métodos permiten a los clientes obtener información sobre los dispositivos de punto de conexión que se encuentran en cualquiera de los Estados que representan las constantes de estado de dispositivo \_ \_ xxx.

Sin embargo, un cliente puede abrir un flujo (por ejemplo, mediante la obtención de una interfaz [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) para el dispositivo) solo en un dispositivo que se encuentra en \_ estado activo de estado de dispositivo \_ .

En el panel de control multimedia de Windows, Mmsys.cpl, se muestran los dispositivos de punto de conexión de audio en el sistema. Al deshabilitar un dispositivo en Mmsys.cpl se oculta el dispositivo de los mecanismos de detección de dispositivos en las API de audio de nivel superior, pero no se invalidan los objetos de secuencia de los que un cliente podría haber creado una instancia antes de que se deshabilitara el dispositivo. Por ejemplo, si un flujo se está reproduciendo en el dispositivo cuando el usuario lo deshabilita en Mmsys.cpl, el flujo sigue reproduciéndose sin interrupciones.

Por el contrario, al deshabilitar un dispositivo en Administrador de dispositivos se quita el dispositivo del sistema de forma eficaz.

Para usar Mmsys.cpl para ver los dispositivos de representación, abra una ventana del símbolo del sistema y escriba el siguiente comando:

**mmsys.cpl de control,, 0**

Para ver los dispositivos de captura, escriba el siguiente comando:

**mmsys.cpl de control,, 1**

Como alternativa, puede ver los dispositivos de representación o los dispositivos de captura en Mmsys.cpl si hace clic con el botón secundario en el icono de altavoz en el área de notificación, que se encuentra en el lado derecho de la barra de tareas, y selecciona **dispositivos de reproducción** o **dispositivos de grabación**.

Mmsys.cpl muestra siempre los dispositivos de punto de conexión que se encuentran en \_ estado activo de estado de dispositivo \_ . Además, se puede configurar para mostrar los dispositivos desconectados y desconectados.

Para ver los dispositivos de punto de conexión que se encuentran en estado de dispositivo \_ \_ deshabilitado y estado de dispositivo \_ \_ NOTPRESENT, haga clic con el botón derecho en la ventana de Mmsys.cpl y seleccione la opción **Mostrar dispositivos deshabilitados** .

Para ver los dispositivos de punto de conexión que se encuentran en estado de dispositivo \_ \_ desconectado, haga clic con el botón derecho en la ventana de Mmsys.cpl y seleccione la opción **Mostrar dispositivos desconectados** .

Para ver solo los dispositivos de punto de conexión que se encuentran en \_ estado activo de estado de dispositivo \_ , anule la selección de las opciones **Mostrar dispositivos deshabilitados** y **Mostrar dispositivos desconectados** .

Para habilitar o deshabilitar un dispositivo de extremo en Mmsys.cpl, haga clic en **reproducción** o **grabación**, en función de si el dispositivo es un dispositivo de reproducción o de grabación. Después, seleccione el dispositivo y haga clic en **propiedades**. En la ventana **propiedades** , junto a **uso del dispositivo**, seleccione **usar este dispositivo (habilitar)** o **no usar este dispositivo (deshabilitar)**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de audio principales](core-audio-constants.md)
</dt> <dt>

[**IMMDevice:: GetState**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-getstate)
</dt> <dt>

[**Interfaz IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> <dt>

[**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints)
</dt> <dt>

[**IMMNotificationClient::OnDeviceStateChanged**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immnotificationclient-ondevicestatechanged)
</dt> </dl>

 

 





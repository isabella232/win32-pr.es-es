---
title: Método IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: Notifica al módulo de redirección de dispositivos Escritorio remoto ActiveX control que se ha producido un cambio de dispositivo en el sistema. Este método pasa notificaciones \_ DE WM DEVICECHANGE al control .
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable
- Interfaz IMsRdpClientNonScriptable Servicios de Escritorio remoto , método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable2
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto , método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , método NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37986a218f672f5ace6d81b6496b958547e70a95f8ddea91bf6a130eb05b1ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130082"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>IMsRdpClientNonScriptable::NotifyRedirectDeviceChange (método)

Notifica al módulo de redirección de dispositivos Escritorio remoto ActiveX control que se ha producido un cambio de dispositivo en el sistema. Este método pasa [**notificaciones DE WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al control .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Especifica el evento de dispositivo. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**


</dt> <dd>

Se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**


</dt> <dd>

La configuración actual ha cambiado debido a un acoplamiento o desacoplado.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**


</dt> <dd>

Se ha producido un evento personalizado.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**


</dt> <dd>

Se ha insertado un dispositivo y ahora está disponible.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**


</dt> <dd>

Se solicita permiso para quitar un dispositivo. Cualquier aplicación puede denegar esta solicitud y cancelar la eliminación.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**


</dt> <dd>

Se ha cancelado una solicitud para quitar un dispositivo.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**


</dt> <dd>

Se ha quitado un dispositivo.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**


</dt> <dd>

Un dispositivo está a punto de quitarse. No se puede denegar la eliminación.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**


</dt> <dd>

Se ha producido un evento específico del dispositivo.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ HA CAMBIADO**


</dt> <dd>

Se ha agregado o quitado un dispositivo del sistema.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ DEFINIDO POR EL USUARIO**


</dt> <dd>

El significado de este mensaje es definido por el usuario.

</dd> </dl> </dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una estructura que contiene datos específicos del evento. Su formato depende del valor del *parámetro wParam.* Para obtener más información, consulte la documentación de cada evento. Para obtener más información, vea [Tipos de eventos de dispositivo.](/windows/desktop/DevIO/device-event-types)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

Una aplicación contenedora que permite la adición o eliminación dinámica de dispositivos debe procesar el mensaje [**\_ DEVICECHANGE de WM**](/windows/desktop/DevIO/wm-devicechange) en su ventana de nivel superior y reenviar el mensaje al control mediante el método **NotifyRedirectDeviceChange.** Un ejemplo de cambio dinámico del dispositivo es cuando se agrega o quita una unidad de disco redirigida mientras se ejecuta el sistema.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                               |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable se define como 2f079c4c-87b2-4afd-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 


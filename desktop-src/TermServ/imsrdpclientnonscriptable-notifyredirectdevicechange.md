---
title: IMsRdpClientNonScriptable NotifyRedirectDeviceChange, método
description: Notifica al módulo de redireccionamiento de dispositivos del Escritorio remoto control ActiveX que se ha producido un cambio de dispositivo en el sistema. Este método pasa \_ las notificaciones de WM DEVICECHANGE al control.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Interfaz IMsRdpClientNonScriptable Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
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
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997055"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>IMsRdpClientNonScriptable:: NotifyRedirectDeviceChange (método)

Notifica al módulo de redireccionamiento de dispositivos del Escritorio remoto control ActiveX que se ha producido un cambio de dispositivo en el sistema. Este método pasa las notificaciones de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al control.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
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

La configuración actual ha cambiado debido a un acoplamiento o desacoplamiento.

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

Se canceló una solicitud para quitar un dispositivo.

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

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ Changed**


</dt> <dd>

Se ha agregado o quitado un dispositivo del sistema.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERDEFINED**


</dt> <dd>

El significado de este mensaje está definido por el usuario.

</dd> </dl> </dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura que contiene datos específicos del evento. Su formato depende del valor del parámetro *wParam* . Para obtener más información, consulte la documentación de cada evento. Para obtener más información, consulte [tipos de eventos de dispositivo](/windows/desktop/DevIO/device-event-types).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

Una aplicación contenedora que permita la adición o eliminación dinámica de dispositivos debe procesar el mensaje de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) en su ventana de nivel superior y reenviar el mensaje al control mediante el método **NotifyRedirectDeviceChange** . Un ejemplo de cambio dinámico de un dispositivo es cuando se agrega o se quita una unidad de disco redirigida mientras el sistema se está ejecutando.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 


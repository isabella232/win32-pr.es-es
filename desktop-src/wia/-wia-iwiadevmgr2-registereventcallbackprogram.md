---
description: 'El método IWiaDevMgr2:: RegisterEventCallbackProgram registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente para la compatibilidad con versiones anteriores de aplicaciones que no se escribieron para la adquisición de imágenes de Windows (WIA) 2,0.'
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: 'IWiaDevMgr2:: RegisterEventCallbackProgram (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackProgram
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b18b5833b7616493c24f0128caa7c910b685e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720390"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>IWiaDevMgr2:: RegisterEventCallbackProgram (método)

El método **IWiaDevMgr2:: RegisterEventCallbackProgram** registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente para la compatibilidad con versiones anteriores de aplicaciones que no se escribieron para la adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEventCallbackProgram(
  [in]       LONG lFlags,
  [in]       BSTR bstrDeviceID,
  [in] const GUID *pEventGUID,
  [in]       BSTR bstrFullAppName,
  [in]       BSTR bstrCommandlineArg,
  [in]       BSTR bstrName,
  [in]       BSTR bstrDescription,
  [in]       BSTR bstrIcon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Marcas de registro. Se puede establecer en los valores siguientes.



| Value                                                                                                                                                                                                           | Significado                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**\_devolución de \_ llamada de evento de registro WIA \_**</dt> </dl>       | Regístrese para el evento.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**devolución de llamada de evento WIA \_ UNregister \_ \_**</dt> </dl> | Elimine el registro del evento.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**\_ \_ controlador predeterminado de WIA set \_**</dt> </dl>                   | Establezca la aplicación como el controlador de eventos predeterminado.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Un identificador de dispositivo. Pase **null** para registrar el evento en todos los dispositivos WIA 2,0.

</dd> <dt>

*pEventGUID* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

Evento para el que se registra la aplicación. Para obtener una lista de GUID de eventos válidos, vea [identificadores de eventos de WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

_bstrFullAppName * \[ en\]
</dt> <dd>

Tipo: **BSTR**

Nombre completo de la ruta de acceso de la aplicación.

</dd> <dt>

*bstrCommandlineArg* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Argumentos de línea de comandos adecuados para la aplicación.

</dd> <dt>

*bstrName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Nombre de la aplicación. El nombre se muestra al usuario cuando se registran varias aplicaciones para el mismo evento.

</dd> <dt>

*bstrDescription* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Descripción de la aplicación. La descripción se muestra al usuario cuando se registran varias aplicaciones para el mismo evento.

</dd> <dt>

*bstrIcon* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Icono que representa la aplicación. El icono se muestra al usuario cuando se registran varias aplicaciones para el mismo evento. La cadena contiene el nombre de la aplicación y el índice de base cero del icono separado por una coma, por ejemplo, "MyApp, 0". Puede haber más de un icono que represente una aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use **IWiaDevMgr2:: RegisterEventCallbackProgram** para registrar eventos de dispositivo de hardware. Cuando se produce un evento en el que se registra una aplicación para, se inicia la aplicación y la información del evento se transmite a la aplicación.

Use el método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para recuperar un puntero a un objeto de enumerador para las propiedades de registro de eventos.

Use el método **IWiaDevMgr2:: RegisterEventCallbackProgram** para mantener la compatibilidad con las aplicaciones no escritas para la arquitectura WIA 2,0. Use las interfaces del modelo de objetos componentes (COM) proporcionadas por la arquitectura WIA 2,0 para las nuevas aplicaciones. En concreto, llame a [**IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) o [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) para registrar una nueva aplicación para eventos de dispositivo.

Normalmente, se llama a este método con un programa de instalación o un script. El programa de instalación o el script registra la aplicación para recibir eventos de dispositivo WIA 2,0. Cuando se produce el evento, el sistema en tiempo de ejecución de WIA 2,0 inicia la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 





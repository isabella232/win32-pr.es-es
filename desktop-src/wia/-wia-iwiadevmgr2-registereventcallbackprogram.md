---
description: El método IWiaDevMgr2::RegisterEventCallbackProgram registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente por compatibilidad con versiones anteriores con aplicaciones que no se escribieron para Windows Image Acquisition (WIA) 2.0.
ms.assetid: 6b427f19-719b-44ce-8e2c-3c44672345c8
title: Método IWiaDevMgr2::RegisterEventCallbackProgram (Wia.h)
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
ms.openlocfilehash: 6ebc99e61bf038c8db2ea537a1f8a5933ad512d21ec05cf51f6f8b7af5ede2b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441303"
---
# <a name="iwiadevmgr2registereventcallbackprogram-method"></a>IWiaDevMgr2::RegisterEventCallbackProgram (método)

El **método IWiaDevMgr2::RegisterEventCallbackProgram** registra una aplicación para recibir eventos de dispositivo. Se proporciona principalmente por compatibilidad con versiones anteriores con aplicaciones que no se escribieron para Windows Image Acquisition (WIA) 2.0.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Marcas de registro. Se puede establecer en los valores siguientes.



| Value                                                                                                                                                                                                           | Significado                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="WIA_REGISTER_EVENT_CALLBACK"></span><span id="wia_register_event_callback"></span><dl> <dt>**DEVOLUCIÓN DE \_ LLAMADA DE EVENTOS DE REGISTRO \_ \_ DE WIA**</dt> </dl>       | Regístrese para el evento.<br/>                           |
| <span id="WIA_UNREGISTER_EVENT_CALLBACK"></span><span id="wia_unregister_event_callback"></span><dl> <dt>**DEVOLUCIÓN DE \_ LLAMADA DE EVENTOS DE \_ ANULACIÓN DEL REGISTRO \_ DE WIA**</dt> </dl> | Elimine el registro del evento.<br/>            |
| <span id="WIA_SET_DEFAULT_HANDLER"></span><span id="wia_set_default_handler"></span><dl> <dt>**WIA \_ SET \_ DEFAULT \_ HANDLER**</dt> </dl>                   | Establezca la aplicación como controlador de eventos predeterminado.<br/> |



 

</dd> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador de dispositivo. Pase **NULL** para registrarse para el evento en todos los dispositivos WIA 2.0.

</dd> <dt>

*pEventGUID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Evento para el que se registra la aplicación. Para obtener una lista de GUID de eventos válidos, vea [Identificadores de eventos de WIA.](-wia-wia-event-identifiers.md)

</dd> <dt>

*bstrFullAppName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Nombre completo de la ruta de acceso de la aplicación.

</dd> <dt>

*bstrCommandlineArg* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Argumentos de línea de comandos adecuados para la aplicación.

</dd> <dt>

*bstrName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Nombre de la aplicación. El nombre se muestra al usuario cuando varias aplicaciones se registran para el mismo evento.

</dd> <dt>

*bstrDescription* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Descripción de la aplicación. La descripción se muestra al usuario cuando varias aplicaciones se registran para el mismo evento.

</dd> <dt>

*bstrIcon* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Icono que representa la aplicación. El icono se muestra al usuario cuando varias aplicaciones se registran para el mismo evento. La cadena contiene el nombre de la aplicación y el índice de base cero del icono separado por una coma, por ejemplo, "MyApp, 0". Puede haber más de un icono que represente una aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Use **IWiaDevMgr2::RegisterEventCallbackProgram para** registrarse para eventos de dispositivo de hardware. Cuando se produce un evento para el que se registra una aplicación, se inicia la aplicación y la información del evento se transmite a la aplicación.

Use el [**método EnumRegisterEventInfo para**](-wia-iwiaitem2-enumregistereventinfo.md) recuperar un puntero a un objeto enumerador para las propiedades de registro de eventos.

Use solo el **método IWiaDevMgr2::RegisterEventCallbackProgram** para la compatibilidad con versiones anteriores con aplicaciones no escritas para la arquitectura WIA 2.0. Use las interfaces del Modelo de objetos componentes (COM) proporcionadas por la arquitectura de WIA 2.0 para las nuevas aplicaciones. En concreto, llame a [**IWiaDevMgr2::RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) o [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) para registrar una nueva aplicación para eventos de dispositivo.

Normalmente, un programa de instalación o un script llama a este método. El programa o script de instalación registra la aplicación para recibir eventos de dispositivo WIA 2.0. Cuando se produce el evento, el sistema en tiempo de ejecución de WIA 2.0 inicia la aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 





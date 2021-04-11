---
description: Registra una aplicación en ejecución para la notificación de eventos de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2:: RegisterEventCallbackInterface (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276855"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2:: RegisterEventCallbackInterface (método)

Registra una aplicación en ejecución para la notificación de eventos de adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrDeviceID* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador único de un dispositivo WIA 2,0. Establezca este parámetro en **null** para registrarse en el evento en todos los dispositivos WIA 2,0.

</dd> <dt>

*pEventGUID* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

Especifica un puntero al identificador de eventos para el que se registra la aplicación. Vea [identificadores de eventos de WIA](-wia-wia-event-identifiers.md) para los identificadores de eventos estándar.

</dd> <dt>

_pIWiaEventCallback * \[ en\]
</dt> <dd>

Tipo: **[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _

Especifica un puntero a la interfaz [_ *IWiaEventCallback* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que WIA 2,0 usa para enviar la notificación de eventos.

</dd> <dt>

*pEventObject* \[ enuncia\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Recibe la dirección de un puntero a la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve los códigos de error COM estándar o los siguientes.



| Código devuelto                                                                               | Descripción                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | No se puede devolver la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . <br/> |



 

## <a name="remarks"></a>Observaciones

> [!WARNING]
> El uso de los métodos [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2:: RegisterEventCallbackInterface** y [**DeviceManager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) del mismo proceso después de que se reinicie el servicio de imágenes fijas puede producir una infracción de acceso, si se usaron las funciones antes de que se detuviera el servicio.

 

Cuando las aplicaciones de WIA 2,0 empiezan a ejecutarse, utilizan este método para registrarse y recibir eventos de dispositivo de hardware. Esto evita que la aplicación se reinicie cuando se produce otro evento para el que se ha registrado. Una vez que una aplicación llama a **IWiaDevMgr2:: RegisterEventCallbackInterface** para registrarse a fin de recibir eventos de WIA 2,0 desde un dispositivo, WIA 2,0 envía los eventos registrados al programa.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *pEventObject* .

> [!Note]  
> En una aplicación multiproceso, la devolución de llamada de notificación de eventos puede entrar en un subproceso diferente del que registró la devolución de llamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

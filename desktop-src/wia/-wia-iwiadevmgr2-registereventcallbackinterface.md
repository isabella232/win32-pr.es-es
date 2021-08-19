---
description: Registra una aplicación en ejecución para la Windows de eventos de adquisición de imágenes (WIA) 2.0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: Método IWiaDevMgr2::RegisterEventCallbackInterface (Wia.h)
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
ms.openlocfilehash: e2658654254257c707d12f4e676aee3371f0ad491dfedeb0637508ca3f33a057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965653"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2::RegisterEventCallbackInterface (método)

Registra una aplicación en ejecución para la Windows de eventos de adquisición de imágenes (WIA) 2.0.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador único de un dispositivo WIA 2.0. Establezca este parámetro en **NULL para** registrarse para el evento en todos los dispositivos WIA 2.0.

</dd> <dt>

*pEventGUID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Especifica un puntero al identificador de evento para el que se está registrando la aplicación. Consulte [Identificadores de eventos de WIA](-wia-wia-event-identifiers.md) para obtener información sobre los identificadores de eventos estándar.

</dd> <dt>

*pIWiaEventCallback* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Especifica un puntero a la interfaz [**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que usa WIA 2.0 para enviar notificaciones de eventos.

</dd> <dt>

*pEventObject* \[ out\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Recibe la dirección de un puntero a la [interfaz IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Devuelve los códigos de error COM estándar o lo siguiente.



| Código devuelto                                                                               | Descripción                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | No se puede devolver la interfaz [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown) <br/> |



 

## <a name="remarks"></a>Comentarios

> [!WARNING]
> El uso de los métodos [**IWiaDevMgr::RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2::RegisterEventCallbackInterface** y [**DeviceManager.RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) desde el mismo proceso después de reiniciar el servicio Still Image puede provocar una infracción de acceso si las funciones se usaron antes de que se detuvo el servicio.

 

Cuando las aplicaciones WIA 2.0 comienzan a ejecutarse, usan este método para registrarse y recibir eventos de dispositivo de hardware. Esto evita que la aplicación se reinicie cuando se produce otro evento para el que está registrada. Una vez que una aplicación llama a **IWiaDevMgr2::RegisterEventCallbackInterface** para registrarse para recibir eventos de WIA 2.0 desde un dispositivo, WIA 2.0 enruta los eventos registrados al programa.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro pEventObject.*

> [!Note]  
> En una aplicación multiproceso, la devolución de llamada de notificación de eventos puede entrar en un subproceso diferente del que registró la devolución de llamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

---
description: 'El método IWiaDevMgr2:: RegisterEventCallbackCLSID registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.'
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: 'IWiaDevMgr2:: RegisterEventCallbackCLSID (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackCLSID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 63e69d12d47f90ba40f5cc785d8b864c40158774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542790"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>IWiaDevMgr2:: RegisterEventCallbackCLSID (método)

El método **IWiaDevMgr2:: RegisterEventCallbackCLSID** registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterEventCallbackCLSID(
  [in]               LONG lFlags,
  [in]               BSTR bstrDeviceID,
  [in]         const GUID *pEventGUID,
  [in, unique] const GUID *pClsID,
  [in]               BSTR bstrName,
  [in]               BSTR bstrDescription,
  [in]               BSTR bstrIcon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica las marcas de registro. Se puede establecer en los siguientes valores:



| Marca de registro                | Significado                                           |
|----------------------------------|---------------------------------------------------|
| \_devolución de \_ llamada de evento de registro WIA \_   | Regístrese para el evento.                           |
| devolución de llamada de evento WIA \_ UNregister \_ \_ | Elimine el registro del evento.            |
| \_ \_ controlador predeterminado de WIA set \_       | Establezca la aplicación como el controlador de eventos predeterminado. |



 

</dd> <dt>

*bstrDeviceID* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica un identificador de dispositivo. Pase **null** para registrar el evento en todos los dispositivos WIA 2,0.

</dd> <dt>

*pEventGUID* \[ de\]
</dt> <dd>

Tipo: **const GUID \** _

Especifica el evento para el que se registra la aplicación. Para obtener una lista de eventos estándar, vea [identificadores de eventos de WIA](-wia-wia-event-identifiers.md).

</dd> <dt>

_pClsID * \[ en\]
</dt> <dd>

Tipo: **const GUID \** _

Puntero al identificador de clase de la aplicación (_ * CLSID * *). El sistema en tiempo de ejecución de WIA 2,0 usa el **CLSID** de la aplicación para iniciar la aplicación cuando se produce un evento para el que se ha registrado.

</dd> <dt>

*bstrName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la aplicación que se registra para el evento.

</dd> <dt>

*bstrDescription* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica una descripción de texto de la aplicación que se registra para el evento.

</dd> <dt>

*bstrIcon* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de un archivo de imagen que se va a utilizar para el icono de la aplicación que se registra para el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las aplicaciones WIA 2,0 usan este método para registrarse y recibir eventos de dispositivo de hardware. Después de llamar a **IWiaDevMgr2:: RegisterEventCallbackCLSID** , la aplicación se registra para recibir eventos de dispositivo WIA 2,0, incluso si no se está ejecutando.

Cuando se produce el evento, el sistema WIA 2,0 determina qué aplicación se registra para recibir el evento. Usa la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y el CLSID especificado en el parámetro *pClsID* para crear una instancia de la aplicación y, a continuación, llama al método [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) para transmitir la información del evento a la aplicación.

Una aplicación puede invocar el método [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para enumerar la información de registro de eventos.

Si la aplicación no es un componente del modelo de objetos componentes (COM) registrado y no es compatible con la arquitectura WIA 2,0, use el método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para registrar una aplicación para eventos de dispositivo.

> [!Note]  
> En una aplicación multiproceso, no hay ninguna garantía de que la devolución de llamada de notificación de eventos se devuelva en el mismo subproceso que registró la devolución de llamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 

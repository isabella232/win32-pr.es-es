---
description: El método IWiaDevMgr2::RegisterEventCallbackCLSID registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.
ms.assetid: e0d421a7-ef49-4e27-9661-c358ac819712
title: Método IWiaDevMgr2::RegisterEventCallbackCLSID (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573184"
---
# <a name="iwiadevmgr2registereventcallbackclsid-method"></a>IWiaDevMgr2::RegisterEventCallbackCLSID (método)

El **método IWiaDevMgr2::RegisterEventCallbackCLSID** registra una aplicación para recibir eventos incluso si la aplicación no se está ejecutando.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica marcas de registro. Se puede establecer en los siguientes valores:



| Marca de registro                | Significado                                           |
|----------------------------------|---------------------------------------------------|
| DEVOLUCIÓN DE \_ LLAMADA DE EVENTOS DE REGISTRO \_ \_ DE WIA   | Regístrese para el evento.                           |
| DEVOLUCIÓN DE \_ LLAMADA DE EVENTOS DE \_ ANULACIÓN DEL REGISTRO \_ DE WIA | Elimine el registro del evento.            |
| CONTROLADOR PREDETERMINADO \_ DE WIA SET \_ \_       | Establezca la aplicación como controlador de eventos predeterminado. |



 

</dd> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica un identificador de dispositivo. Pase **NULL** para registrarse para el evento en todos los dispositivos WIA 2.0.

</dd> <dt>

*pEventGUID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Especifica el evento para el que se registra la aplicación. Para obtener una lista de eventos estándar, vea [Identificadores de eventos de WIA.](-wia-wia-event-identifiers.md)

</dd> <dt>

*pClsID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Puntero al identificador de clase de aplicación (**CLSID**). El sistema en tiempo de ejecución de WIA 2.0 usa el **CLSID** de la aplicación para iniciar la aplicación cuando se produce un evento para el que está registrada.

</dd> <dt>

*bstrName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la aplicación que se registra para el evento.

</dd> <dt>

*bstrDescription* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica una descripción de texto de la aplicación que se registra para el evento.

</dd> <dt>

*bstrIcon* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de un archivo de imagen que se usará para el icono de la aplicación que se registra para el evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Las aplicaciones WIA 2.0 usan este método para registrarse y recibir eventos de dispositivo de hardware. Después de llamar a **IWiaDevMgr2::RegisterEventCallbackCLSID,** la aplicación se registra para recibir eventos de dispositivo WIA 2.0 incluso si no se está ejecutando.

Cuando se produce el evento, el sistema WIA 2.0 determina qué aplicación está registrada para recibir el evento. Usa la función [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) y el CLSID especificado en el parámetro *pClsID* para crear una instancia de la aplicación y, a continuación, llama al método [**ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) para transmitir la información del evento a la aplicación.

Una aplicación puede invocar el [**método EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) para enumerar la información de registro de eventos.

Si la aplicación no es un componente registrado del Modelo de objetos componentes (COM) y no es compatible con la arquitectura de WIA 2.0, use el método [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) para registrar una aplicación para eventos de dispositivo.

> [!Note]  
> En una aplicación multiproceso, no hay ninguna garantía de que la devolución de llamada de notificación de eventos se devuelva en el mismo subproceso que registró la devolución de llamada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 

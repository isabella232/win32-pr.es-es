---
title: Interfaz IMsRdpClientAdvancedSettings2
description: Administra la configuración avanzada del cliente. Deriva de la interfaz IMsRdpClientAdvancedSettings.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97584aa3b37adc148672777e95fe0b2c8b101e09989bfa1ab5debbffe489640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001413"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a>Interfaz IMsRdpClientAdvancedSettings2

Administra la configuración avanzada del cliente. Deriva de la [**interfaz IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) Esta interfaz incluye métodos para recuperar y establecer propiedades avanzadas (opcionales) para el Escritorio remoto ActiveX control.

Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **\_ IID IMsRdpClientAdvancedSettings2** a **QueryInterface**.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientAdvancedSettings2** hereda de [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md). **IMsRdpClientAdvancedSettings2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientAdvancedSettings2** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso           | Descripción                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanAutoReconnect**](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | Solo lectura<br/>  | Especifica si el control de cliente puede volver a conectarse automáticamente a la sesión actual en caso de desconexión de red.<br/>    |
| [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | Lectura/escritura<br/> | Especifica si se debe permitir que el control de cliente se vuelva a conectar automáticamente a una sesión en caso de desconexión de red.<br/>            |
| [**MaxReconnectAttempts**](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | Lectura/escritura<br/> | Especifica el número de veces que se intenta volver a conectar durante la reconexión automática. Los valores válidos de esta propiedad son de 0 a 200 inclusive.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz se ha ampliado mediante las interfaces siguientes, y cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings2 se define como 9ac42117-2b76-4320-aa44-0e616ab8437b<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


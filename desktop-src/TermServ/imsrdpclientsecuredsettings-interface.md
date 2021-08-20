---
title: Interfaz IMsRdpClientSecuredSettings
description: Incluye métodos para recuperar y establecer las propiedades del control Escritorio remoto ActiveX que están restringidas a zonas de seguridad de Internet Explorer URL específicas. | Interfaz IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a1b834d42c957998ad2a8eda5cd3790dd16f40dfd82a8e463bc34e510cd742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129795"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Interfaz IMsRdpClientSecuredSettings

Incluye métodos para recuperar y establecer las propiedades del control Escritorio remoto ActiveX que están restringidas a zonas de seguridad de Internet Explorer URL específicas.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientSecuredSettings** hereda de [**IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md) **IMsRdpClientSecuredSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientSecuredSettings** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lectura/escritura<br/> | La configuración de redireccionamiento de audio.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lectura/escritura<br/> | La configuración de redireccionamiento del teclado.<br/> |



 

## <a name="remarks"></a>Comentarios

Estas propiedades no se pueden establecer cuando el control está conectado.

Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre los métodos de esta interfaz.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-a811-068fb7be346d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 






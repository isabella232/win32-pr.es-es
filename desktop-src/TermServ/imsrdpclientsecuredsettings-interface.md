---
title: Interfaz IMsRdpClientSecuredSettings
description: Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer. | Interfaz IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, descrito
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
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678711"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Interfaz IMsRdpClientSecuredSettings

Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientSecuredSettings** hereda de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md). **IMsRdpClientSecuredSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientSecuredSettings** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lectura/escritura<br/> | La configuración de redirección de audio.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lectura/escritura<br/> | La configuración de redirección del teclado.<br/> |



 

## <a name="remarks"></a>Observaciones

Estas propiedades no se pueden establecer cuando el control está conectado.

Consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre los métodos de esta interfaz.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 






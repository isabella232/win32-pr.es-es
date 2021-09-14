---
title: Interfaz IMsTscSecuredSettings
description: Incluye métodos para recuperar y establecer las propiedades del control Escritorio remoto ActiveX que están restringidas a zonas de seguridad Internet Explorer URL específicas. | Interfaz IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Interfaz IMsTscSecuredSettings Servicios de Escritorio remoto
- Interfaz IMsTscSecuredSettings Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168713"
---
# <a name="imstscsecuredsettings-interface"></a>Interfaz IMsTscSecuredSettings

Incluye métodos para recuperar y establecer las propiedades del control Escritorio remoto ActiveX que están restringidas a zonas de seguridad Internet Explorer URL específicas. Las propiedades incluyen las que especifican el modo del control de cliente (modo de pantalla completa o modo de ventana) y el programa que se inicia al conectarse al servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto). Estos métodos también están disponibles a través de [**la interfaz IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md)

## <a name="members"></a>Members

La **interfaz IMsTscSecuredSettings** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsTscSecuredSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsTscSecuredSettings** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**Fullscreen**](imstscsecuredsettings-fullscreen.md)<br/>     | Lectura y escritura<br/> | Estado de pantalla completa del control de cliente.<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | Lectura y escritura<br/> | Programa que se va a iniciar en el servidor remoto tras la conexión.<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | Lectura y escritura<br/> | Directorio de trabajo del programa de inicio.<br/>                     |



 

## <a name="remarks"></a>Observaciones

Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre los métodos de esta interfaz.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


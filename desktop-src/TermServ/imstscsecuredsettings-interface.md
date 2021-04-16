---
title: Interfaz IMsTscSecuredSettings
description: Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer. | Interfaz IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings, descrito
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689760"
---
# <a name="imstscsecuredsettings-interface"></a>Interfaz IMsTscSecuredSettings

Incluye métodos para recuperar y establecer las propiedades del control ActiveX Escritorio remoto que están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer. Las propiedades incluyen las que especifican el modo del control de cliente (modo de pantalla completa o modo de ventana) y el programa que se va a iniciar tras la conexión al servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto). Estos métodos también están disponibles a través de la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .

## <a name="members"></a>Miembros

La interfaz **IMsTscSecuredSettings** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscSecuredSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsTscSecuredSettings** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**FullScreen**](imstscsecuredsettings-fullscreen.md)<br/>     | Lectura/escritura<br/> | El estado de pantalla completa del control de cliente.<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | Lectura/escritura<br/> | Programa que se va a iniciar en el servidor remoto después de la conexión.<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | Lectura/escritura<br/> | Directorio de trabajo del programa de inicio.<br/>                     |



 

## <a name="remarks"></a>Observaciones

Consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información sobre los métodos de esta interfaz.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


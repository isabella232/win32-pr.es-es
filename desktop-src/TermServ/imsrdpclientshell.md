---
title: IMsRdpClientShell (interfaz)
description: Conexión a Escritorio remoto configuración de cliente (RDC) que se usa para iniciar el cliente desde Escritorio remoto Web Access (Acceso web de Escritorio remoto) o desde otros portales web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientShell Servicios de Escritorio remoto
- Interfaz de IMsRdpClientShell Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8593a890097bbfaf6d9c9876bb56d92794ce204f38f349c72beb73b8d28403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621035"
---
# <a name="imsrdpclientshell-interface"></a>IMsRdpClientShell (interfaz)

Conexión a Escritorio remoto configuración de cliente (RDC) que se usa para iniciar el cliente desde Escritorio remoto Web Access (Acceso web de Escritorio remoto) o desde otros portales web.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientShell** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpClientShell** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpClientShell** tiene estos métodos.



| Método                                                     | Descripción                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Recupera una sola propiedad RDP.<br/>                  |
| [**Lanzamiento**](imsrdpclientshell-launch.md)                 | Inicia el contenido del archivo remoto desde el portal web.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Establece una sola propiedad RDP.<br/>                       |



 

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientShell** tiene estas propiedades.



| Propiedad                                                                                              | Tipo de acceso           | Descripción                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Solo lectura<br/>  | Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad RemoteApp.<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lectura/escritura<br/> | Recupera si el modo público está habilitado.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lectura/escritura<br/> | Versión de secuencia del archivo de configuración de RDP.<br/>                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpClientShell se define como \_ d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


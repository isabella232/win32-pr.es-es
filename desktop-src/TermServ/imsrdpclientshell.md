---
title: Interfaz IMsRdpClientShell
description: La configuración de cliente Conexión a Escritorio remoto (RDC) que se usa para iniciar el cliente desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell, descrito
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
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491650"
---
# <a name="imsrdpclientshell-interface"></a>Interfaz IMsRdpClientShell

La configuración de cliente Conexión a Escritorio remoto (RDC) que se usa para iniciar el cliente desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientShell** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsRdpClientShell** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpClientShell** tiene estos métodos.



| Método                                                     | Descripción                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| [**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85)) | Recupera una sola propiedad de RDP.<br/>                  |
| [**Launch**](imsrdpclientshell-launch.md)                 | Inicia el contenido del archivo remoto desde el portal web.<br/> |
| [**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85)) | Establece una única propiedad de RDP.<br/>                       |



 

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientShell** tiene estas propiedades.



| Propiedad                                                                                              | Tipo de acceso           | Descripción                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**IsRemoteProgramClientInstalled**](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | Solo lectura<br/>  | Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad de RemoteApp.<br/> |
| [**PublicMode**](imsrdpclientshell-publicmode.md)<br/>                                         | Lectura/escritura<br/> | Recupera si está habilitado el modo público.<br/>                                                      |
| [**RdpFileContents**](imsrdpclientshell-rdpfilecontents.md)<br/>                               | Lectura/escritura<br/> | Versión de Stream del archivo de configuración de RDP.<br/>                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell se define como d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


---
title: Interfaz IMsRdpWorkspace
description: Expone métodos que administran Conexión de RemoteApp y Escritorio credenciales y conexiones.
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpWorkspace Servicios de Escritorio remoto
- Interfaz IMsRdpWorkspace Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1489690632b0ef1bf05a529d84ed5c96afb6c442c82744f964c9a89e9286299d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125535"
---
# <a name="imsrdpworkspace-interface"></a>Interfaz IMsRdpWorkspace

Expone métodos que administran Conexión de RemoteApp y Escritorio credenciales y conexiones. Esta interfaz se implementa mediante el Servicios de Escritorio remoto web Access Control. Este control es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución de Conexiones de Escritorio y RemoteApp (Tswbprxy.exe).

## <a name="members"></a>Miembros

La **interfaz IMsRdpWorkspace** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsRdpWorkspace** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpWorkspace** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))             | Elimina las credenciales de usuario asociadas al identificador de conexión especificado.<br/>                                                                                  |
| [**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))                       | Desconecta todas las conexiones existentes asociadas al identificador de conexión especificado y elimina las credenciales de usuario correspondientes del almacén de credenciales.<br/> |
| [**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85)) | Determina si existen credenciales de usuario para el identificador de conexión especificado.<br/>                                                                                 |
| [**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))                   | Determina si el inicio de sesión único (SSO) está habilitado para Conexión de RemoteApp y Escritorio.<br/>                                                                   |
| [**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))                               | Marca la autenticación de las credenciales de usuario para el identificador de conexión y, posteriormente, muestra la notificación de conexión en el área de notificación de la barra de tareas. <br/>     |
| [**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))                                 | Asocia las credenciales de usuario y los certificados a un identificador de conexión.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpWorkspace se define como \_ 145D0621-04CF-4FC2-A766-A81A9069CDF8<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 


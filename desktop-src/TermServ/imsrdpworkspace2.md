---
title: Interfaz IMsRdpWorkspace2
description: Expone un método que asocia Conexión de RemoteApp y Escritorio credenciales a una conexión.
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
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
ms.openlocfilehash: 38b869d3ffc83d9a4b8f3d51df0b7b14658ec3f1c561797a62dee3a574bf2803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125525"
---
# <a name="imsrdpworkspace2-interface"></a>Interfaz IMsRdpWorkspace2

Expone un método que asocia Conexión de RemoteApp y Escritorio credenciales a una conexión. Esta interfaz se implementa mediante el Servicios de Escritorio remoto web Access Control. Este control es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución de Conexiones de Escritorio y RemoteApp (Tswbprxy.exe).

## <a name="members"></a>Miembros

La **interfaz IMsRdpWorkspace** hereda de [**IMsRdpWorkspace**](imsrdpworkspace.md). **IMsRdpWorkspace2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpWorkspace** tiene estos métodos.



| Método                                                        | Descripción                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85)) | Asocia las credenciales de usuario y los certificados a un identificador de conexión. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpWorkspace2 se define como 145D0622-04CF-4FC3-A776-A82A9169CDF8<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 


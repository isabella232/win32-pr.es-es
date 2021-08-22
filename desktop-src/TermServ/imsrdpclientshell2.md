---
title: Interfaz IMsRdpClientShell2
description: Expone las propiedades que inician Conexión a Escritorio remoto cliente desde Escritorio remoto Web Access (Acceso web de Escritorio remoto) o desde otros portales web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientShell2 Servicios de Escritorio remoto
- Interfaz IMsRdpClientShell2 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e9a63e631ca88575f4b632def5e47b29b68da414d48af95d42e757dcb2da6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138658"
---
# <a name="imsrdpclientshell2-interface"></a>Interfaz IMsRdpClientShell2

Expone las propiedades que inician Conexión a Escritorio remoto cliente desde Escritorio remoto Web Access (Acceso web de Escritorio remoto) o desde otros portales web.

Esta interfaz se implementa mediante Servicios de Escritorio remoto Web Access Control, que es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución remoteapp y conexiones de escritorio (Tswbprxy.exe).

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientShell2** hereda de **IMsRdpClientShell.** **IMsRdpClientShell2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientShell2** tiene estas propiedades.



| Propiedad                                                                               | Tipo de acceso          | Descripción                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Solo lectura<br/> | Recupera un puntero a la [**interfaz IMsRdpWorkspace,**](imsrdpworkspace.md) que se usa para administrar Conexión de RemoteApp y Escritorio credenciales y conexiones.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Solo lectura<br/> | Recupera un valor que indica si la página web actual está en una zona de seguridad de Internet Explorer url de confianza.<br/>                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 






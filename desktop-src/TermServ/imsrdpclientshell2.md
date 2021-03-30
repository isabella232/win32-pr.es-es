---
title: Interfaz IMsRdpClientShell2
description: Expone propiedades que inician el cliente de Conexión a Escritorio remoto desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2, descrito
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
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801562"
---
# <a name="imsrdpclientshell2-interface"></a>Interfaz IMsRdpClientShell2

Expone propiedades que inician el cliente de Conexión a Escritorio remoto desde Escritorio remoto Web Access (acceso web de escritorio remoto) o desde otros portales web.

Esta interfaz la implementa Servicios de Escritorio remoto Web Access Control, que es un contenedor alrededor del cliente de Conexión a Escritorio remoto (MsTscAx.dll) y el proxy en tiempo de ejecución de conexiones de RemoteApp y escritorio (Tswbprxy.exe).

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientShell2** hereda de **IMsRdpClientShell**. **IMsRdpClientShell2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientShell2** tiene estas propiedades.



| Propiedad                                                                               | Tipo de acceso          | Descripción                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MsRdpWorkspace**](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | Solo lectura<br/> | Recupera un puntero a la interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) , que se usa para administrar conexión de RemoteApp y escritorio credenciales y conexiones.<br/> |
| [**SecuredSettingsEnabled**](imsrdpclientshell2-securedsettingsenabled.md)<br/> | Solo lectura<br/> | Recupera un valor que indica si la página web actual está en una zona de seguridad de direcciones URL de Internet Explorer de confianza.<br/>                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpWorkspace**](imsrdpworkspace.md)
</dt> </dl>

 

 






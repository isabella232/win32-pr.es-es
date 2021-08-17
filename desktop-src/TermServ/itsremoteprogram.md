---
title: Interfaz ITSRemoteProgram
description: Incluye métodos para establecer y recuperar el modo RemoteApp y los parámetros de inicio de un programa RemoteApp, como la ruta de acceso del archivo ejecutable y el directorio de trabajo.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Interfaz ITSRemoteProgram Servicios de Escritorio remoto
- Interfaz ITSRemoteProgram Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b719771f265347da59ce4d8c5990a5b9dc5a72315780def0fd3a34b108e18169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756814"
---
# <a name="itsremoteprogram-interface"></a>Interfaz ITSRemoteProgram

Incluye métodos para establecer y recuperar el modo RemoteApp y los parámetros de inicio de un programa RemoteApp, como la ruta de acceso del archivo ejecutable y el directorio de trabajo.

## <a name="members"></a>Miembros

La **interfaz ITSRemoteProgram** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITSRemoteProgram también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz ITSRemoteProgram** tiene estos métodos.



| Método                                                            | Descripción                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**ServerStartProgram**](itsremoteprogram-serverstartprogram.md) | Especifica un programa RemoteApp que se iniciará en la sesión remota.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz ITSRemoteProgram** tiene estas propiedades.



| Propiedad                                                                   | Tipo de acceso           | Descripción                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | Lectura/escritura<br/> | Modo RemoteApp.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram se define como \_ FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


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
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968144"
---
# <a name="itsremoteprogram-interface"></a>Interfaz ITSRemoteProgram

Incluye métodos para establecer y recuperar el modo RemoteApp y los parámetros de inicio de un programa RemoteApp, como la ruta de acceso del archivo ejecutable y el directorio de trabajo.

## <a name="members"></a>Members

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
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | Lectura y escritura<br/> | El modo RemoteApp.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram se define como \_ FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 


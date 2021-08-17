---
title: Método MoveDown de la Win32_TSGatewayRADIUSServer clase
description: Mueve este servidor Servicio de autenticación remota telefónica de usuario (RADIUS) una posición hacia abajo en el orden de prioridad.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- Método MoveDown Servicios de Escritorio remoto
- Método MoveDown Servicios de Escritorio remoto , Win32_TSGatewayRADIUSServer clase
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto método , MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acee402af28ed62c5f4627972b083d1fd5c3ed7f49b02a058fb4f2562ffbd681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138179"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a>Método MoveDown de la clase \_ TSGatewayRADIUSServer de Win32

Mueve este servidor Servicio de autenticación remota telefónica de usuario (RADIUS) una posición hacia abajo en el orden de prioridad. Este método incrementa la **propiedad Priority** del servidor RADIUS actual y disminuye la propiedad **Priority** del servidor RADIUS que sigue al servidor RADIUS actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 MoveDown();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayRADIUSServer de Win32 \_**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


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
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968116"
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

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TSGatewayRADIUSServer de Win32 \_**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


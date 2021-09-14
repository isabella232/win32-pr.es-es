---
title: Método MoveUp de la Win32_TSGatewayRADIUSServer clase
description: Mueve esta Servicio de autenticación remota telefónica de usuario servidor (RADIUS) una posición hacia arriba en el orden de prioridad.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- Método MoveUp Servicios de Escritorio remoto
- Método MoveUp Servicios de Escritorio remoto , Win32_TSGatewayRADIUSServer clase
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto método , MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968104"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a>Método MoveUp de la clase \_ TSGatewayRADIUSServer de Win32

Mueve esta Servicio de autenticación remota telefónica de usuario servidor (RADIUS) una posición hacia arriba en el orden de prioridad. Este método disminuye la propiedad **Priority** del servidor RADIUS actual e incrementa la propiedad **Priority** del servidor RADIUS que precede al servidor RADIUS actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 MoveUp();
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

 


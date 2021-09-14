---
title: Método Disconnect de la Win32_TSGatewayConnection clase
description: Desconecta la conexión del servidor Escritorio remoto gateway (puerta de enlace de Escritorio remoto).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- Método disconnect Servicios de Escritorio remoto
- Método Disconnect Servicios de Escritorio remoto , Win32_TSGatewayConnection clase
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto método , Disconnect
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891121"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a>Método Disconnect de la clase \_ TSGatewayConnection de Win32

Desconecta la conexión del servidor Escritorio remoto gateway (puerta de enlace de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Disconnect();
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

[**TSGatewayConnection de Win32 \_**](win32-tsgatewayconnection.md)
</dt> </dl>

 


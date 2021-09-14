---
title: Método Update de la clase Win32_TSGatewayRADIUSServer actualización
description: Actualiza el servidor Servicio de autenticación remota telefónica de usuario (RADIUS) actual.
ms.assetid: 38a15768-66eb-40d6-a079-16555f2bf96a
ms.tgt_platform: multiple
keywords:
- Actualizar método Servicios de Escritorio remoto
- Actualizar método Servicios de Escritorio remoto , Win32_TSGatewayRADIUSServer clase
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto , Método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4faf0c87e49a507ac300d7e8b32f218ed006ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890881"
---
# <a name="update-method-of-the-win32_tsgatewayradiusserver-class"></a>Método Update de la clase \_ TSGatewayRADIUSServer de Win32

Actualiza el servidor Servicio de autenticación remota telefónica de usuario (RADIUS) actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Update(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del servidor RADIUS.

</dd> <dt>

*SharedSecret* \[ En\]
</dt> <dd>

Secreto compartido para el servidor RADIUS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


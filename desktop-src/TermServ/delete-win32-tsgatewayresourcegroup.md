---
title: Método Delete de la Win32_TSGatewayResourceGroup clase
description: Elimina el grupo de recursos.
ms.assetid: 669a24b1-4828-498d-b249-7e9725d9bf72
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto , Win32_TSGatewayResourceGroup clase
- Win32_TSGatewayResourceGroup clase Servicios de Escritorio remoto método , Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9123b7f63238cdb2007ecea49aaf0bca236a7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073346"
---
# <a name="delete-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método Delete de la clase \_ TSGatewayResourceGroup de Win32

Elimina el grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Observaciones

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

[**TSGatewayResourceGroup de Win32 \_**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 


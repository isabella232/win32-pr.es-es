---
title: Método MoveUp de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Mueve la directiva de autorización Escritorio remoto conexión actual (Escritorio remoto \ 160; CAP) una posición hacia arriba en el orden en que Rd \ 160; Se evalúan las CAP.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- Método MoveUp Servicios de Escritorio remoto
- Método MoveUp Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto , método MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968107"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método MoveUp de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Mueve la directiva Escritorio remoto autorización de conexión (CAP de Escritorio remoto) actual una posición hacia arriba en el orden en que se evalúan las CA de Escritorio remoto. Este método disminuye la propiedad **Order** del CAP de Escritorio remoto actual e incrementa la propiedad **Order** del CAP de Escritorio remoto que precedía al CAP de Escritorio remoto actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


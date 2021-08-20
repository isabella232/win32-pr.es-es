---
title: Método SetEnabled de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece la propiedad Enabled, que habilita o deshabilita la directiva de autorización de Servicios de Escritorio remoto de conexión actual (Escritorio remoto \ 160; CAP).
ms.assetid: f8c0b39e-95d4-46cf-83fb-e91b650fbb4d
ms.tgt_platform: multiple
keywords:
- Método SetEnabled Servicios de Escritorio remoto
- Método SetEnabled Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto , método SetEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb25fff49962d019a01605c8392c3a09f1029152f6aed0ec8809302a81895408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000475"
---
# <a name="setenabled-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetEnabled de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece la **propiedad Enabled,** que habilita o deshabilita la directiva de autorización Servicios de Escritorio remoto conexión actual (CAP de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitado* \[ En\]
</dt> <dd>

**True** si se va a habilitar el CAP de Escritorio remoto, **False** si se va a deshabilitar el CAP de Escritorio remoto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, devuelve cero. Si el método no es correcto, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


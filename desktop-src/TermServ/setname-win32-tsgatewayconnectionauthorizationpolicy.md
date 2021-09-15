---
title: Método SetName de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece un nuevo nombre para esta directiva Escritorio remoto de autorización de conexión (Escritorio remoto \ 160; CAP).
ms.assetid: 4a3b71d4-9b1c-46ea-b14a-fcbe32af37b5
ms.tgt_platform: multiple
keywords:
- Método SetName Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto método , SetName
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15fa4c374f5686f8cddbe99b5a464e6f84b4a12a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258956"
---
# <a name="setname-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetName de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece un nuevo nombre para esta directiva Escritorio remoto de autorización de conexión (CAP de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del CAP de Escritorio remoto. El nombre debe tener 64 caracteres o menos, ser único (se omite case) y no puede contener los siguientes caracteres reservados:

<> : ; " / \\ \| ? \*\[TAB\]

</dd> </dl>

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

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


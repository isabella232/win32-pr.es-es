---
title: Método MoveUp de la clase Win32_TSGatewayConnectionAuthorizationPolicy
description: Mueve la Directiva de autorización de conexión Escritorio remoto actual (RD \ 160; CAP) una posición hacia arriba en el orden en que RD \ 160; Se evalúan los extremos.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- MoveUp (método) Servicios de Escritorio remoto
- Método MoveUp Servicios de Escritorio remoto, clase Win32_TSGatewayConnectionAuthorizationPolicy
- Clase Win32_TSGatewayConnectionAuthorizationPolicy Servicios de Escritorio remoto, método MoveUp
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492988"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método MoveUp de la \_ clase TSGatewayConnectionAuthorizationPolicy de Win32

Mueve la Directiva de autorización de conexión de Escritorio remoto actual una posición hacia arriba en el orden en que se evalúan las Cap de RD. Este método reduce la propiedad **Order** de la Cap de RD actual e incrementa la propiedad **Order** de la Cap de RD que precedía a la Cap de RD actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 MoveUp();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Bajar**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


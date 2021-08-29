---
title: Método SetSessionTimeout de la Win32_TSGatewayConnectionAuthorizationPolicy clase
description: Establece las propiedades SessionTimeout y SessionTimeoutAction.
ms.assetid: 11491c97-3ef8-46c1-9504-696c613e374e
ms.tgt_platform: multiple
keywords:
- Método SetSessionTimeout Servicios de Escritorio remoto
- Método SetSessionTimeout Servicios de Escritorio remoto , Win32_TSGatewayConnectionAuthorizationPolicy clase
- Win32_TSGatewayConnectionAuthorizationPolicy clase Servicios de Escritorio remoto , método SetSessionTimeout
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSessionTimeout
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c786372628fa272f9d3f2a3486034a6339b94e3b658b184b74a5a31fc11f492e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865105"
---
# <a name="setsessiontimeout-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método SetSessionTimeout de la clase \_ TSGatewayConnectionAuthorizationPolicy de Win32

Establece las **propiedades SessionTimeout** **y SessionTimeoutAction.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSessionTimeout(
  [in] uint32 SessionTimeout,
  [in] uint32 SessionTimeoutAction
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SessionTimeout* \[ En\]
</dt> <dd>

Tipo: **uint32**

El nuevo valor de tiempo de espera, en minutos. Un valor de 0 significa que no hay tiempo de espera.

</dd> <dt>

*SessionTimeoutAction* \[ En\]
</dt> <dd>

Tipo: **uint32**

Especifica la acción que se debe realizar en caso de que se agote el tiempo de espera de la sesión. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

Desconecte la sesión.

</dd> <dt>

1
</dt> <dd>

Intente volver a autorizar la sesión.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


---
title: Método EnumAuthorizationPlugins de la Win32_TSGatewayServerSettings clase
description: Enumera todos los complementos de autorización registrados.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Método EnumAuthorizationPlugins Servicios de Escritorio remoto
- Método EnumAuthorizationPlugins Servicios de Escritorio remoto , Win32_TSGatewayServerSettings clase
- Win32_TSGatewayServerSettings clase Servicios de Escritorio remoto método , EnumAuthorizationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40447b6befd3042c766b4bd312619563617119b114c329867bfc3ca0b3e7bfce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574635"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnumAuthorizationPlugins de la clase \_ TSGatewayServerSettings de Win32

Enumera todos los complementos de autorización registrados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PluginNames* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz **de** cadenas que recibe los nombres de los complementos de autorización registrados.

</dd> <dt>

*CLSID* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz **de** cadenas que recibe los CLID de los complementos de autorización registrados.

</dd> <dt>

*Descripciones* \[ out\]
</dt> <dd>

Tipo: **\[ \] cadena**

Matriz **de** cadenas que recibe las descripciones de los complementos de autorización registrados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si el método se realiza correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentarios

Debe ser miembro del grupo Administradores para llamar a este método.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSGatewayServerSettings de Win32 \_**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


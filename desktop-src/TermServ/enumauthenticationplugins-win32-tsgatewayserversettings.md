---
title: Método EnumAuthenticationPlugins de la clase Win32_TSGatewayServerSettings
description: Enumera todos los complementos de autenticación registrados.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Método EnumAuthenticationPlugins Servicios de Escritorio remoto
- Método EnumAuthenticationPlugins Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676644"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnumAuthenticationPlugins de la \_ clase TSGatewayServerSettings de Win32

Enumera todos los complementos de autenticación registrados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PluginNames* \[ enuncia\]
</dt> <dd>

Tipo: **String \[ \]**

Una matriz de **cadena** que recibe los nombres de los complementos de autenticación registrados.

</dd> <dt>

*CLSID* \[ enuncia\]
</dt> <dd>

Tipo: **String \[ \]**

Una matriz de **cadena** que recibe los CLSID de los complementos de autenticación registrados.

</dd> <dt>

*Descripciones* \[ enuncia\]
</dt> <dd>

Tipo: **String \[ \]**

Una matriz de **cadena** que recibe las descripciones de los complementos de autenticación registrados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Si el método se ejecuta correctamente, devuelve cero. Si el método no se realiza correctamente, devuelve un valor distinto de cero. Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Para llamar a este método, debe ser miembro del grupo administradores.

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                        |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 


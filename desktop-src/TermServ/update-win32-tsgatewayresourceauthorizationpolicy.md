---
title: Método Update de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Actualiza la Directiva de autorización de recursos de Escritorio remoto actual (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Método Update Servicios de Escritorio remoto
- Método Update Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Servicios de Escritorio remoto de clase Win32_TSGatewayResourceAuthorizationPolicy, método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904d5fa092cddfbfda1c94f1810a6f6da1a9a8a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150486"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método Update de la \_ clase Win32 TSGatewayResourceAuthorizationPolicy

Actualiza la Directiva de autorización de recursos de Escritorio remoto actual (RAP de RD).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ de de\]
</dt> <dd>

Nombre de la RAP de RD.

</dd> <dt>

*Descripción* \[ de de\]
</dt> <dd>

Descripción de la RAP de RD.

</dd> <dt>

*Habilitado* \[ de\]
</dt> <dd>

Indica si se debe habilitar la RAP de RD.

</dd> <dt>

*ResourceGroupName* \[ de\]
</dt> <dd>

Nombre del grupo de recursos asociado a esta RAP de RD.

</dd> <dt>

*ResourceGroupType* \[ de\]
</dt> <dd>

Tipo de grupo de recursos.

<dt>

RG
</dt> <dd>

Un grupo de recursos

</dd> <dt>

CG
</dt> <dd>

Grupo de equipos, tal como se almacena en Active Directory Domain Services.

</dd> <dt>

TODOS
</dt> <dd>

Todos los recursos.

</dd> </dl> </dd> <dt>

*UserGroupNames* \[ de\]
</dt> <dd>

Lista separada por puntos y comas de nombres de grupos de usuarios. Los nombres tienen el formato *dominio \\ UserGroupName*. Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso.

</dd> <dt>

*ProtocolNames* \[ de\]
</dt> <dd>

Lista separada por puntos y comas de nombres de protocolo que están habilitados para esta Directiva. Los nombres deben coincidir con el valor devuelto del método [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) de la clase [**\_ TSGatewayServerSettings de Win32**](win32-tsgatewayserversettings.md) .

</dd> <dt>

*PortNumbers* \[ de\]
</dt> <dd>

Lista separada por puntos y comas de números de puerto que están habilitados para esta Directiva. Para permitir cualquier número de puerto, establezca " \* ".

</dd> </dl>

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

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


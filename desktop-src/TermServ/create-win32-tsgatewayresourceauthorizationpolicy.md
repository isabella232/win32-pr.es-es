---
title: Método Create de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Crea una directiva de autorización de recursos de Escritorio remoto (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Crear método Servicios de Escritorio remoto
- Create Method Servicios de Escritorio remoto, Win32_TSGatewayResourceAuthorizationPolicy (clase)
- Win32_TSGatewayResourceAuthorizationPolicy Servicios de Escritorio remoto de clase, Create (método)
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422023"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método Create de la \_ clase Win32 TSGatewayResourceAuthorizationPolicy

Crea una directiva de autorización de recursos de Escritorio remoto (RAP de RD).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
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

Indica si se va a habilitar la RAP de RD.

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

*ResourceGroupName* \[ de\]
</dt> <dd>

Nombre del grupo de recursos.

</dd> <dt>

*UserGroupNames* \[ de\]
</dt> <dd>

Lista separada por puntos y comas de nombres de grupos de usuarios. Si el usuario pertenece a alguno de estos grupos de usuarios, se permitirá el acceso. Los nombres de grupos de usuarios deben tener el formato *dominio \\ UserGroupName*.

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

 


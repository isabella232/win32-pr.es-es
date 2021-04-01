---
title: Método SetResourceGroup de la clase Win32_TSGatewayResourceAuthorizationPolicy
description: Establece el tipo y el nombre del grupo de recursos.
ms.assetid: a3dd0ffa-a39b-46f9-8317-fcc90a8afcd1
ms.tgt_platform: multiple
keywords:
- Método SetResourceGroup Servicios de Escritorio remoto
- Método SetResourceGroup Servicios de Escritorio remoto, clase Win32_TSGatewayResourceAuthorizationPolicy
- Win32_TSGatewayResourceAuthorizationPolicy de clase Servicios de Escritorio remoto, método SetResourceGroup
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetResourceGroup
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22c2ceacbbbfc40372d0f0d084cf6525f754934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905412"
---
# <a name="setresourcegroup-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Método SetResourceGroup de la \_ clase TSGatewayResourceAuthorizationPolicy de Win32

Establece el tipo y el nombre del grupo de recursos.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetResourceGroup(
  [in] string ResourceGroupName,
  [in] string ResourceGroupType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ResourceGroupName* \[ de\]
</dt> <dd>

Nombre del grupo de recursos. Este valor reemplaza la propiedad **ResourceGroupName** existente.

</dd> <dt>

*ResourceGroupType* \[ de\]
</dt> <dd>

Identifica el tipo del grupo de recursos. Este valor reemplaza la propiedad **ResourceGroupType** existente.

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

</dd> </dl> </dd> </dl>

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

 


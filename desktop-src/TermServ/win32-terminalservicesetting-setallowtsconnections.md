---
title: Método SetAllowTSConnections de la clase Win32_TerminalServiceSetting
description: El método SetAllowTSConnections permite o deniega nuevas conexiones de escritorio remoto. Este método modificará la propiedad AllowTSConnections de la clase en consecuencia.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Método SetAllowTSConnections Servicios de Escritorio remoto
- Método SetAllowTSConnections Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492725"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Método SetAllowTSConnections de la \_ clase TerminalServiceSetting de Win32

El método **SetAllowTSConnections** permite o deniega nuevas conexiones de escritorio remoto. Este método modificará la propiedad **AllowTSConnections** de la clase en consecuencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AllowTSConnections* \[ de\]
</dt> <dd>

Especifica si se permiten las nuevas conexiones de escritorio remoto. Debe ser uno de los valores siguientes.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

No se permiten nuevas conexiones. Si el parámetro *ModifyFirewallException* es 1, la excepción de firewall de escritorio remoto está deshabilitada.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Se permiten nuevas conexiones. Si el parámetro *ModifyFirewallException* es 1, la excepción de firewall de escritorio remoto está habilitada.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ de\]
</dt> <dd>

Especifica si el valor de la excepción de Firewall para Escritorio remoto se modificará al estado especificado por el parámetro *AllowTSConnections* . Debe ser uno de los valores siguientes.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

No modifique la configuración de excepción del firewall.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modifique la configuración de la excepción del firewall.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve SUCCESS si se realiza correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 


---
title: Método SetAllowTSConnections de la Win32_TerminalServiceSetting clase
description: El método SetAllowTSConnections permite o deniega nuevas conexiones a Escritorio remoto. Este método modificará la propiedad AllowTSConnections para la clase en consecuencia.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Método SetAllowTSConnections Servicios de Escritorio remoto
- Método SetAllowTSConnections Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetAllowTSConnections
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
ms.openlocfilehash: 63f8e9be06a19599f578089fa979d7fd93a7bf457fcadf033ed0ab56fea4947f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127031"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Método SetAllowTSConnections de la clase \_ TerminalServiceSetting de Win32

El **método SetAllowTSConnections** permite o deniega nuevas conexiones a Escritorio remoto. Este método modificará la **propiedad AllowTSConnections** para la clase en consecuencia.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AllowTSConnections* \[ En\]
</dt> <dd>

Especifica si se permiten nuevas conexiones a Escritorio remoto. Debe ser uno de los siguientes valores.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

No se permiten nuevas conexiones. Si el *parámetro ModifyFirewallException* es 1, la excepción Escritorio remoto firewall está deshabilitada.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Se permiten nuevas conexiones. Si el *parámetro ModifyFirewallException* es 1, la excepción Escritorio remoto firewall está habilitada.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ En\]
</dt> <dd>

Especifica si la configuración de excepción de firewall Escritorio remoto se modificará al estado especificado por el *parámetro AllowTSConnections.* Debe ser uno de los siguientes valores.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

No modifique la configuración de excepción del firewall.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modifique la configuración de excepción del firewall.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 


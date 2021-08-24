---
title: Método CreateWinstation de la Win32_TerminalServiceSetting clase
description: Crea una nueva pila de agentes de escucha basada en la combinación única de nombre de agente de escucha y NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Método CreateWinstation Servicios de Escritorio remoto
- Método CreateWinstation Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc78266d18b73ee31634a0fc33a244aea3dd9b30d5f6c65c5d646b7aa3da0de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681405"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a>Método CreateWinstation de la clase TerminalServiceSetting de Win32 \_

El **método CreateWinstation crea** una nueva pila de agentes de escucha basada en la combinación única de nombre de agente de escucha y NIC.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nombre del agente de escucha.

</dd> <dt>

*WinstaDriverName* \[ En\]
</dt> <dd>

Nombre del controlador winstation.

</dd> <dt>

*LanaId* \[ En\]
</dt> <dd>

Número del adaptador de red de área local (LANA) de NetBIOS para la NIC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 


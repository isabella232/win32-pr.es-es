---
title: Método SelectNetworkAdapterIP de la Win32_TSNetworkAdapterSetting clase
description: Selecciona un adaptador de red basado en la dirección IP del adaptador.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Selección del método SelectNetworkAdapterIP Servicios de Escritorio remoto
- Método SelectNetworkAdapterIP Servicios de Escritorio remoto , Win32_TSNetworkAdapterSetting clase
- Win32_TSNetworkAdapterSetting clase Servicios de Escritorio remoto , método SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9590bab26b3cda2e20a3dc74c5e201a2f7f86f94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243464"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SelectNetworkAdapterIP de la clase \_ TSNetworkAdapterSetting de Win32

Selecciona un adaptador de red basado en la dirección IP del adaptador.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NetworkAdapterIP* \[ En\]
</dt> <dd>

Dirección IP del adaptador de red que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si la dirección IP especificada es válida y devuelve un código de error WMI si la dirección IP no es válida o no existe. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Puede recuperar la dirección IP de un adaptador de red enumerando las propiedades de la clase [**\_ TSNetworkAdapterListSetting de Win32.**](win32-tsnetworkadapterlistsetting.md)

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_TSNetworkAdapterSetting de Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 


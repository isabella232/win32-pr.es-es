---
title: Método SetNetworkAdapterLanaID de la Win32_TSNetworkAdapterSetting clase
description: Especifica el número de adaptador de red de área local (LANA) del adaptador de red que se establecerá.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Método SetNetworkAdapterLanaID Servicios de Escritorio remoto
- Método SetNetworkAdapterLanaID Servicios de Escritorio remoto , Win32_TSNetworkAdapterSetting clase
- Win32_TSNetworkAdapterSetting clase Servicios de Escritorio remoto método , SetNetworkAdapterLanaID
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SetNetworkAdapterLanaID
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5ffe976da794714f01e711913c01216d6b9bfad30c8c337da1fbd4c796e5f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008965"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SetNetworkAdapterLanaID de la clase \_ TSNetworkAdapterSetting de Win32

El **método SetNetworkAdapterLanaID** especifica el número de adaptador de red de área local (LANA) del adaptador de red que se establecerá. Si el identificador de LANA especificado no es válido o no existe, se devuelve un error. La lista disponible de los id. de LANA se obtiene enumerando la propiedad **DeviceIDList** en la clase [**\_ TSNetworkAdapterSetting de Win32.**](win32-tsnetworkadaptersetting.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NetworkAdapterLanaID* \[ En\]
</dt> <dd>

Número LANA del adaptador de red que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

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

 


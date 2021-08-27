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
ms.openlocfilehash: bb4a88c4820e4537d9c0fb1833b67eb2660a7fb5618189023dfe2217f222efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008375"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SelectNetworkAdapterIP de la clase \_ Win32 TSNetworkAdapterSetting

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

## <a name="remarks"></a>Comentarios

Puede recuperar la dirección IP de un adaptador de red enumerando las propiedades de la clase [**\_ TSNetworkAdapterListSetting de Win32.**](win32-tsnetworkadapterlistsetting.md)

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 


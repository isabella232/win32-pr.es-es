---
title: Método SelectNetworkAdapterIP de la clase Win32_TSNetworkAdapterSetting
description: Selecciona un adaptador de red basado en la dirección IP del adaptador.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Método SelectNetworkAdapterIP Servicios de Escritorio remoto
- Método SelectNetworkAdapterIP Servicios de Escritorio remoto, clase Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de clase Servicios de Escritorio remoto, método SelectNetworkAdapterIP
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685955"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SelectNetworkAdapterIP de la \_ clase TSNetworkAdapterSetting de Win32

Selecciona un adaptador de red basado en la dirección IP del adaptador.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NetworkAdapterIP* \[ de\]
</dt> <dd>

Dirección IP del adaptador de red que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si la dirección IP especificada es válida y devuelve un código de error de WMI si la dirección IP no es válida o no existe. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Puede recuperar la dirección IP de un adaptador de red mediante la enumeración de las propiedades de la clase [**\_ TSNetworkAdapterListSetting de Win32**](win32-tsnetworkadapterlistsetting.md) .

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

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 


---
title: Método SetNetworkAdapterLanaID de la clase Win32_TSNetworkAdapterSetting
description: Especifica el número de adaptador de red de área local (LANA) del adaptador de red que se va a establecer.
ms.assetid: a12c7f06-4ecf-40bd-98c5-a2583dd1754a
ms.tgt_platform: multiple
keywords:
- Método SetNetworkAdapterLanaID Servicios de Escritorio remoto
- Método SetNetworkAdapterLanaID Servicios de Escritorio remoto, clase Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de clase Servicios de Escritorio remoto, método SetNetworkAdapterLanaID
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
ms.openlocfilehash: 00675ae6378041e6c06b82a7de3c1ccf27620f4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803770"
---
# <a name="setnetworkadapterlanaid-method-of-the-win32_tsnetworkadaptersetting-class"></a>Método SetNetworkAdapterLanaID de la \_ clase TSNetworkAdapterSetting de Win32

El método **SetNetworkAdapterLanaID** especifica el número de adaptador de red de área local (lana) del adaptador de red que se va a establecer. Si el ID. de LANA especificado no es válido o no existe, se devuelve un error. La lista de identificadores de LANA disponible se obtiene enumerando la propiedad **DeviceIDList** en la clase [**\_ TSNetworkAdapterSetting de Win32**](win32-tsnetworkadaptersetting.md) .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetNetworkAdapterLanaID(
  [in] uint32 NetworkAdapterLanaID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NetworkAdapterLanaID* \[ de\]
</dt> <dd>

Número LANA del adaptador de red que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

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

[**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 


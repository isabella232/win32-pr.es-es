---
title: Método SelectNetworkAdapter de la Win32_TSVirtualIP clase
description: Establece la dirección MAC del adaptador de red que se usará para la virtualización de IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Método SelectNetworkAdapter Servicios de Escritorio remoto
- Método SelectNetworkAdapter Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto , método SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374518"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a>Método SelectNetworkAdapter de la clase \_ TSVirtualIP de Win32

Establece la dirección MAC del adaptador de red que se usará para la virtualización de IP.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NetworkAdapterMacAddress* \[ En\]
</dt> <dd>

Tipo: **cadena**

Especifica la dirección MAC del adaptador de red.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

Si la dirección MAC no es válida o no existe, o si el modo de virtualización IP es por sesión, se devuelve un error.

El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                       |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSVirtualIP de Win32 \_**](win32-tsvirtualip.md)
</dt> </dl>

 

 






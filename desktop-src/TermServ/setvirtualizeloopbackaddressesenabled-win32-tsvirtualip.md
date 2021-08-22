---
title: Método SetVirtualizeLoopbackAddressesEnabled de la Win32_TSVirtualIP clase
description: Establece el valor de la propiedad VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Método SetVirtualizeLoopbackAddressesEnabled Servicios de Escritorio remoto
- Método SetVirtualizeLoopbackAddressesEnabled Servicios de Escritorio remoto , Win32_TSVirtualIP clase
- Win32_TSVirtualIP clase Servicios de Escritorio remoto , método SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5168ddd271dcf013a7595be1e1bdf32cde91e8f9f3ce8cfebc3b9f39af1fa109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000495"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualizeLoopbackAddressesEnabled de la \_ clase TSVirtualIP de Win32

Establece el **valor de la propiedad VirtualizeLoopbackAddressesEnabled.**

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[ En\]
</dt> <dd>

Especifica si se debe habilitar la virtualización de direcciones de bucle atrás. Puede ser uno de los siguientes valores.

<dt>

0
</dt> <dd>

No habilite la virtualización de direcciones de bucle atrás.

</dd> <dt>

1
</dt> <dd>

Habilitación de la virtualización de direcciones de bucle atrás.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 






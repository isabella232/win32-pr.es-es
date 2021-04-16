---
title: Método SetVirtualizeLoopbackAddressesEnabled de la clase Win32_TSVirtualIP
description: Establece el valor de la propiedad VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Método SetVirtualizeLoopbackAddressesEnabled Servicios de Escritorio remoto
- Método SetVirtualizeLoopbackAddressesEnabled Servicios de Escritorio remoto, clase Win32_TSVirtualIP
- Win32_TSVirtualIP de clase Servicios de Escritorio remoto, método SetVirtualizeLoopbackAddressesEnabled
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
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676629"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a>Método SetVirtualizeLoopbackAddressesEnabled de la \_ clase TSVirtualIP de Win32

Establece el valor de la propiedad **VirtualizeLoopbackAddressesEnabled** .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VirtualizeLoopbackAddressesEnabled* \[ de\]
</dt> <dd>

Especifica si se va a habilitar la virtualización de la dirección de bucle invertido. Puede ser uno de los valores siguientes.

<dt>

0
</dt> <dd>

No habilite la virtualización de direcciones de bucle invertido.

</dd> <dt>

1
</dt> <dd>

Habilitar la virtualización de direcciones de bucle invertido.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 






---
description: Obtiene las propiedades especificadas de este Plug and Play dispositivo.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Método GetDeviceProperties de la Win32_PnPEntity clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 855c3c0644d8c7b5c5300c8d12d5a6f98073a4511f8d0d65f4058da7fb9d0f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077515"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Método GetDeviceProperties de la clase \_ Win32 PnPEntity

Obtiene las propiedades especificadas de este Plug and Play dispositivo.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*devicePropertyKeys* \[ in, opcional\]
</dt> <dd>

Propiedades que se devuelven.

</dd> <dt>

*deviceProperties* \[ out\]
</dt> <dd>

Las propiedades solicitadas en los subtipos adecuados de [**la clase abstracta \_ PnPDeviceProperty de Win32.**](win32-pnpdeviceproperty.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)
</dt> </dl>

 

 





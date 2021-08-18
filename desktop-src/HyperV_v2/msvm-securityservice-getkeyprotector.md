---
description: Recupera el protector de clave para un sistema virtual.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Método GetKeyProtector de la Msvm_SecurityService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8a7c7768b696f67fd52466eadf8b8487c2c64a7badd86e94b4ef8ff5964e4026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997055"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a>Método GetKeyProtector de la clase SecurityService de Msvm \_

Recupera el protector de clave para un sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecuritySettingData* \[ En\]
</dt> <dd>

String contiene una instancia incrustada de la [**clase \_ SecuritySettingData de Msvm**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.

</dd> <dt>

*KeyProtector* \[ out\]
</dt> <dd>

Recibe la matriz de bytes sin formato que contiene el protector de clave actualmente en uso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 o 4096. De lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1703 \[ solo para aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 





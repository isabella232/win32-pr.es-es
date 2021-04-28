---
description: 'Método SetSecurityPolicy de la clase Msvm_SecurityService : establece el protector de clave para un sistema virtual.'
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Método SetSecurityPolicy de la Msvm_SecurityService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31b03ee8a941b0715b85f6a749c4ba59ade032f7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118733"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a>Método SetSecurityPolicy de la clase SecurityService de Msvm \_

Establece el protector de clave para un sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecuritySettingData* \[ En\]
</dt> <dd>

String contiene una instancia incrustada de la [**clase \_ SecuritySettingData de Msvm**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.

</dd> <dt>

*SecurityPolicy* \[ En\]
</dt> <dd>

Matriz de bytes sin formato que contiene la directiva de seguridad que se establece.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

On, success, devuelve un valor de 0; de lo contrario, devuelve un error.

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

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SecurityService de Msvm \_**](msvm-securityservice.md)
</dt> </dl>

 

 





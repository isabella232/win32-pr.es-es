---
description: Restaura de nuevo al último protector de clave válido conocido.
ms.assetid: 0d1ea5d8-d25e-400c-be65-afe1bd65b1f0
title: Método RestoreLastKnownGoodKeyProtector de la clase Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.RestoreLastKnownGoodKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e82fb3b40f4b85e74f92ed2690a411932af2eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689575"
---
# <a name="restorelastknowngoodkeyprotector-method-of-the-msvm_securityservice-class"></a>Método RestoreLastKnownGoodKeyProtector de la \_ clase SecurityService de MSVM

Restaura de nuevo al último protector de clave válido conocido.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RestoreLastKnownGoodKeyProtector(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SecuritySettingData* \[ de\]
</dt> <dd>

String contiene una instancia incrustada de la clase [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa la configuración de seguridad de un sistema virtual.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente. Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0 o 4096; de lo contrario, devuelve un error.

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

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 





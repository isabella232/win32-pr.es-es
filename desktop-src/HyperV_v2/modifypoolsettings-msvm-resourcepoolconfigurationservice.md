---
description: Cambia la configuración de un grupo secundario que no está relacionado con la asignación.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Método ModifyPoolSettings de la clase Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277991"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método ModifyPoolSettings de la \_ clase ResourcePoolConfigurationService de MSVM

Cambia la configuración de un grupo secundario que no está relacionado con la asignación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ChildPool* \[ de\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ResourcePool de CIM**](cim-resourcepool.md) que representa el grupo secundario que se va a modificar.

</dd> <dt>

*PoolSettings* \[ de\]
</dt> <dd>

Instancia insertada de la clase [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que se usa para especificar la nueva configuración para el grupo.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Trabajo completado sin errores** (0)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

**En uso** (32774)
</dt> <dt>

**Estado no válido** (32775)
</dt> <dt>

**Tipo de recurso incorrecto para el grupo** (32776)
</dt> <dt>

**No disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**Proveedor reservado** (32779)
</dt> <dt>

**Recursos insuficientes** (32780)
</dt> <dt>

**No se encontró el objeto** (32781.. 32787)
</dt> <dt>

**Existe el objeto** (32788)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 


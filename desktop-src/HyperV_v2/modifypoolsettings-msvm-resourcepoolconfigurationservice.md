---
description: Cambia la configuración de un grupo secundario que no está relacionado con la asignación.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Método ModifyPoolSettings de la Msvm_ResourcePoolConfigurationService clase
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
ms.openlocfilehash: e1c8d71f8f380d5049d6bd2743e1f1d48573407431372c53aaeaacf4297ec56e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694045"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método ModifyPoolSettings de la clase ResourcePoolConfigurationService de Msvm \_

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

*ChildPool* \[ En\]
</dt> <dd>

Referencia a una instancia de la clase [**\_ ResourcePool de CIM**](cim-resourcepool.md) que representa el grupo secundario que se debe modificar.

</dd> <dt>

*PoolSettings* \[ En\]
</dt> <dd>

Instancia incrustada de la [**clase \_ ResourcePoolSettingData de Msvm**](msvm-resourcepoolsettingdata.md) que se usa para especificar la nueva configuración del grupo.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Trabajo completado sin error** (0)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**Desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**En uso** (32774)
</dt> <dt>

**Estado no** válido (32775)
</dt> <dt>

**Tipo de recurso incorrecto para el grupo** (32776)
</dt> <dt>

**No disponible** (32777)
</dt> <dt>

**Memoria no suficiente** (32778)
</dt> <dt>

**Vendor Reserved** (32779)
</dt> <dt>

**Recursos insuficientes** (32780)
</dt> <dt>

**Objeto no encontrado** (32781..32787)
</dt> <dt>

**Objeto existe** (32788)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 


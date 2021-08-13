---
description: Inicie un trabajo para crear un subgrupo a partir de un grupo primario con la configuración de asignación especificada.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Método CreateChildResourcePool de la CIM_ResourcePoolConfigurationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 48a43baeefcbc56707fa6327930d9c18eaa57a2442b81fbc5f5cff17633b2148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648157"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método CreateChildResourcePool de la clase \_ ResourcePoolConfigurationService de CIM

Inicie un trabajo para crear un subgrupo a partir de un grupo primario con la configuración de asignación especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ElementName* \[ En\]
</dt> <dd>

Nombre pertinente del usuario final para el grupo que se va a crear. Si **es NULL,** se puede usar un nombre predeterminado proporcionado por el sistema. El valor se almacenará en la **propiedad ElementName** del elemento creado.

</dd> <dt>

*Configuración* \[ En\]
</dt> <dd>

Cadena que contiene una representación de una instancia [**\_ settingData**](cim-settingdata.md) de CIM que se usa para especificar la configuración del grupo secundario.

</dd> <dt>

*ParentPool* \[ En\]
</dt> <dd>

Grupo [**\_ de recursos CIM desde**](cim-resourcepool.md) el que se va a crear el nuevo grupo.

</dd> <dt>

*Grupo* \[ out\]
</dt> <dd>

Grupo [**de recursos DE CIM \_ que**](cim-resourcepool.md) hace referencia al grupo resultante.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Referencia al trabajo (puede ser NULL si el trabajo se ha completado).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Trabajo completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Desconocido** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Parámetro no válido** (5)
</dt> <dt>

**En uso** (6)
</dt> <dt>

**ResourceType incorrecto para el grupo** (7)
</dt> <dt>

**Recursos insuficientes** (8)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Tamaño no admitido** (4097)
</dt> <dt>

**Método reservado** (4098..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 





---
description: Hace referencia a la información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911030"
---
# <a name="msvm_compatibilityvector-class"></a>MSVM \_ CompatibilityVector (clase)

Hace referencia a la información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ CompatibilityVector** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ CompatibilityVector** tiene estas propiedades.

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la operación de comparación que devolverá True si y solo si dos vectores son compatibles. Los datos de la máquina virtual están en el lado izquierdo de la comparación y los datos del host están en el lado derecho.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Igual** (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**Supraconjunto** (1)


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**Subconjunto** (2)


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

**Disjuntos** (3)


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4)


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5)


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**Lessthan** (6)


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7)


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**Múltiplo** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisible** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los datos del atributo de compatibilidad real que se usan para la comparación.

</dd> <dt>

**VectorId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica un vector de compatibilidad que representa un atributo concreto. Esta propiedad se usa para hacer coincidir los vectores correspondientes entre un host y una máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El método [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) de la clase [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) devuelve una matriz de instancias de **MSVM \_ CompatibilityVector** para el host (si se ejecuta en el host) o una máquina virtual (si se ejecuta en la máquina virtual). Cada **entrada \_ CompatibilityVector de MSVM** de la lista describe un vector de atributo de compatibilidad. Para que una máquina virtual sea compatible con un host, todos sus atributos de compatibilidad deben ser compatibles con los atributos de host s.

Cada entrada de **\_ CompatibilityVector de MSVM** tiene estas propiedades:

<dl> <dt>

**VectorId**
</dt> <dd>

Identifica de forma única el vector de compatibilidad. Se usa para hacer coincidir los vectores que se van a comparar entre un host y una máquina virtual.

</dd> <dt>

**CompareOperation**
</dt> <dd>

Identifica la operación de comparación que determina si los vectores son compatibles.

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

Contiene el atributo de compatibilidad real; Esto es, de hecho, la carga del atributo (por ejemplo, la máscara de características del procesador, el tamaño del vaciado de la línea de caché, etc.)

</dd> </dl>

El conjunto de operaciones definido para **CompareOperation** solo implica la comparación de enteros básica y la lógica bit a bit. Esto permite que el contenido real de **CompatibilityInfo** siga siendo opaco. El conjunto de operaciones incluye:



| CompareOperation | Descripción                                      | Comparación de pseudocódigo                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr debe ser igual a HostAttr                       | Si (VmAttr = = HostAttr)              |
| VmCcSuperSet     | VmAttr debe ser un superconjunto de HostAttr            | If ((VmAttr & HostAttr) = = HostAttr) |
| VmCcSubSet       | VmAttr debe ser un subconjunto de HostAttr              | If ((VmAttr & HostAttr) = = VmAttr)   |
| VmCcDisjointSet  | VmAttr debe ser un conjunto separado de HostAttr      | If ((VmAttr & HostAttr) = = 0)        |
| VmCcGreater      | VmAttr debe ser mayor que HostAttr             | If (VmAttr > HostAttr)            |
| VmCcGreaterEqual | VmAttr debe ser mayor o igual que HostAttr | If (VmAttr >= HostAttr)           |
| VmCcLess         | VmAttr debe ser menor que HostAttr                | If (VmAttr < HostAttr)            |
| VmCcLessEqual    | VmAttr debe ser menor o igual que HostAttr    | If (VmAttr <= HostAttr)           |
| VmCcMultiple     | VmAttr debe ser un múltiplo de HostAttr            | If ((VmAttr% HostAttr) = = 0)        |
| VmCcDivisor      | VmAttr debe ser un divisor de HostAttr             | If ((HostAttr% VmAttr) = = 0)        |



 

SCVMM debe realizar estos pasos para determinar si una máquina virtual es compatible con un host.

**Para determinar si una máquina virtual es compatible con un host**

1.  Recorra en iteración todos los elementos **\_ CompatibilityVector de MSVM** para la máquina virtual.
2.  Para cada **elemento \_ CompatibilityVector de MSVM** , use la operación de compatibilidad especificada en **CompareOperation** para comparar el vector de compatibilidad de hardware de la máquina virtual con el vector de compatibilidad correspondiente para el host.
3.  Si todos los elementos **\_ CompatibilityVector de MSVM** de la máquina virtual se consideran compatibles, la máquina virtual es compatible con el host (desde una perspectiva de características del procesador).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





---
description: Hace referencia a la información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un sistema de equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector clase
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
ms.openlocfilehash: 976e6b7bd9bf69e483b987da4d8055ffc102e89c67ed83bab6aa09c4e586b1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531845"
---
# <a name="msvm_compatibilityvector-class"></a>Clase Msvm \_ CompatibilityVector

Hace referencia a la información de compatibilidad de una máquina virtual (VM) (cuando se ejecuta en un sistema de equipo de máquina virtual) o un host (cuando se ejecuta en un sistema de equipo host).

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

La **clase \_ CompatibilityVector de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ CompatibilityVector** tiene estas propiedades.

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la operación de comparación que devolverá true si y solo si dos vectores son compatibles. Los datos de la máquina virtual están en el lado izquierdo de la comparación y los datos del host están en el lado derecho.

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**Igual** (0)


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**Superconjunto** (1)


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**Subconjunto** (2)


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

**Disjoint** (3)


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4)


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5)


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**LessThan** (6)


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7)


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**Varios** (8)


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

**Divisible** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los datos de atributo de compatibilidad reales que se usan para la comparación.

</dd> <dt>

**VectorId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica un vector de compatibilidad que representa un atributo específico. Esta propiedad se usa para hacer coincidir los vectores correspondientes entre un host y una máquina virtual.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El [**método GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) de la clase [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) devuelve una matriz de instancias de **Msvm \_ CompatibilityVector** para el host (si se ejecuta en el host) o una máquina virtual (si se ejecuta en la máquina virtual). Cada **entrada \_ CompatibilityVector de Msvm** de la lista describe un vector de atributo de compatibilidad. Para que una máquina virtual sea compatible con un host, todos sus atributos de compatibilidad deben ser compatibles con los atributos del host.

Cada **entrada \_ CompatibilityVector de Msvm** tiene estas propiedades:

<dl> <dt>

**VectorId**
</dt> <dd>

Identifica de forma única el vector de compatibilidad. Esto se usa para hacer coincidir los vectores que se comparan entre un host y una máquina virtual.

</dd> <dt>

**CompareOperation**
</dt> <dd>

Identifica la operación de comparación que determina si los vectores son compatibles.

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

Contiene el atributo de compatibilidad real; Se trata de la carga útil del atributo (por ejemplo, máscara de características del procesador, tamaño de vaciado de línea de caché, etc.).

</dd> </dl>

El conjunto de operaciones definidas para **CompareOperation solo** implica la comparación básica de enteros y la lógica bit a bit. Esto permite que el contenido real de **CompatibilityInfo** permanezca opaco. El conjunto de operaciones incluye:



| CompareOperation | Descripción                                      | Comparación de pseudocódigos                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr debe ser igual a HostAttr                       | If (VmAttr == HostAttr)              |
| VmCcSuperSet     | VmAttr debe ser un superconjunto de HostAttr            | If ((VmAttr & HostAttr) == HostAttr) |
| VmCcSubSet       | VmAttr debe ser un subconjunto de HostAttr              | If ((VmAttr & HostAttr) == VmAttr)   |
| VmCcDisjointSet  | VmAttr debe ser un conjunto no conjunto de HostAttr      | If ((VmAttr & HostAttr) == 0)        |
| VmCcGreater      | VmAttr debe ser mayor que HostAttr             | If (VmAttr > HostAttr)            |
| VmCcGreaterEqual | VmAttr debe ser mayor o igual que HostAttr | If (VmAttr >= HostAttr)           |
| VmCcLess         | VmAttr debe ser menor que HostAttr                | If (VmAttr < HostAttr)            |
| VmCcLessEqual    | VmAttr debe ser menor o igual que HostAttr    | If (VmAttr <= HostAttr)           |
| VmCcMultiple     | VmAttr debe ser un múltiplo de HostAttr            | Si ((VmAttr % HostAttr) == 0)        |
| VmCcDivisor      | VmAttr debe ser un divisor de HostAttr             | If ((HostAttr % VmAttr) == 0)        |



 

SCVMM debe realizar estos pasos para determinar si una máquina virtual es compatible con un host.

**Para determinar si una máquina virtual es compatible con un host**

1.  Itera todos los elementos **\_ CompatibilityVector de Msvm** para la máquina virtual.
2.  Para cada **elemento \_ CompatibilityVector de Msvm,** use la operación de compatibilidad especificada en **CompareOperation** para comparar el vector de compatibilidad de hardware de la máquina virtual con el vector de compatibilidad correspondiente para el host.
3.  Si todos los elementos **\_ CompatibilityVector de Msvm** de la máquina virtual se consideran compatibles, la máquina virtual es compatible con el host (desde la perspectiva de la característica del procesador).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





---
description: Establecer los datos que se pasarán como una matriz a la clase \_ CollectionReferencePointExportSettingData de Msvm.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Msvm_VirtualMachineToDisks clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b24c99d4e4c066122dbc26c79433668cd965a2bdcce13e3ceb319fb23a954fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899035"
---
# <a name="msvm_virtualmachinetodisks-class"></a>Clase \_ VirtualMachineToDisks de Msvm

Establecer los datos que se pasarán como una matriz a la clase [**\_ CollectionReferencePointExportSettingData de Msvm.**](msvm-collectionreferencepointexportsettingdata.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualMachineToDisks de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VirtualMachineToDisks de Msvm** tiene estas propiedades.

<dl> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los identificadores de instancia wmi de los discos que pertenecen a un identificador de máquina virtual determinado para el que se deben exportar los datos.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Identificador de máquina virtual al que están asociados los discos virtuales.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 





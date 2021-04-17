---
description: Se usa en el método QueryGuestClusterInformation de la \_ clase MSVM VssService para recuperar información sobre el clúster invitado del que forma parte la máquina virtual.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686953"
---
# <a name="msvm_guestclusterinformation-class"></a>MSVM \_ GuestClusterInformation (clase)

Se usa en el método [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) de la clase [**MSVM \_ VssService**](msvm-vssservice.md) para recuperar información sobre el clúster invitado del que forma parte la máquina virtual.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ GuestClusterInformation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ GuestClusterInformation** tiene estas propiedades.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El identificador del clúster de conmutación por error del que forma parte el sistema operativo invitado de la máquina virtual.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de nodos del clúster del que forma parte el sistema operativo invitado de la máquina virtual.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado se comparte entre las máquinas virtuales en modo activo/activo.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el disco correspondiente es un recurso de clúster en el clúster invitado.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado está en línea.

</dd> <dt>

**IsOwned**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Matriz de valores booleanos que corresponden a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado es Currenly propiedad de esta máquina virtual.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El contador del reloj cuando uno de los recursos del disco compartido se desplazó por última vez.

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Una matriz de rutas de acceso de disco duro virtual compartidas conectadas a la máquina virtual.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Una matriz de datos de configuración de asignación de recursos (RASD) que representa los discos duros virtuales compartidos conectados a la máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


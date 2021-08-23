---
description: Se usa en el método QueryGuestClusterInformation de la clase VssService de Msvm para recuperar información sobre el clúster invitado del que forma parte la máquina \_ virtual.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation clase
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
ms.openlocfilehash: ed353e0d9c4d3049e120b00a11bc3d1bf85e3a0b42e52deb4ed277b9bde9b96b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523305"
---
# <a name="msvm_guestclusterinformation-class"></a>Clase Msvm \_ GuestClusterInformation

Se usa en [**el método QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) de la clase [**\_ VssService de Msvm**](msvm-vssservice.md) para recuperar información sobre el clúster invitado del que forma parte la máquina virtual.

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

La **clase \_ GuestClusterInformation de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ GuestClusterInformation** tiene estas propiedades.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El identificador del clúster de conmutación por error del sistema operativo invitado de la máquina virtual forma parte de .

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de nodos del clúster del que forma parte el sistema operativo invitado de la máquina virtual.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de valores booleanos correspondientes a cada disco duro virtual compartido que indica si el recurso de disco correspondiente del clúster invitado se comparte entre máquinas virtuales en modo activo/activo.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de valores booleanos correspondientes a cada disco duro virtual compartido que indica si el disco correspondiente es un recurso de clúster en el clúster invitado.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de valores booleanos correspondientes a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado está en línea.

</dd> <dt>

**IsOwned**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz booleana**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de valores booleanos correspondientes a cada disco duro virtual compartido que indica si el recurso de disco correspondiente en el clúster invitado es propiedad de esta máquina virtual.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Recuento de tics de reloj cuando uno de los recursos de disco compartido se movió por última vez.

> [!Note]  
> Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de rutas de acceso de disco duro virtual compartidas conectadas a la máquina virtual.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de datos de configuración de asignación de recursos (RASD) que representan los discos duros virtuales compartidos conectados a la máquina virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


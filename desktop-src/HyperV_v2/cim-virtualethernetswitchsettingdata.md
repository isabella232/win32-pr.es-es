---
description: Describe los datos de configuración de un conmutador Ethernet virtual.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: CIM_VirtualEthernetSwitchSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6243e86ec53213f959ea0b8f420543a9dca619de9d12593a73619aab2805091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646463"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>Cim \_ VirtualEthernetSwitchSettingData (clase)

Describe los datos de configuración de un conmutador Ethernet virtual.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ VirtualEthernetSwitchSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM VirtualEthernetSwitchSettingData** tiene estas propiedades.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene los grupos de recursos de host que están asociados actualmente, o para asociar con el conmutador Ethernet, con el fin de asignar conexiones Ethernet entre el conmutador Ethernet y una máquina virtual. Cada valor distinto de NULL de esta propiedad debe ajustarse a **WBEM \_ URI \_ UntypedInstancePath** tal como se define en la especificación DMTF "DSP0207".

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de direcciones MAC únicas que el conmutador puede aprender para el aprendizaje de direcciones MAC, tal como se define en el estándar IEEE 802.1.

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene los identificadores de VLAN a los que puede acceder el conmutador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 





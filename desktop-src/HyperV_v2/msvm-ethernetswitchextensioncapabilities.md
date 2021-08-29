---
description: Representa la asociación entre las extensiones Ethernet y sus funcionalidades.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Msvm_EthernetSwitchExtensionCapabilities clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22ff1cd8d720dcb42ae71b1155b7cd69dbc8d098f0cd8ad799f1d47c448c8c63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148351"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a>Clase Msvm \_ EthernetSwitchExtensionCapabilities

Representa la asociación entre las extensiones Ethernet y sus funcionalidades.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchExtensionCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchExtensionCapabilities** tiene estas propiedades.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Funcionalidades")
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa el objeto capabilities asociado al conmutador. Esta propiedad se hereda del [**elemento \_ CIMCapabilities.**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)

</dd> <dt>

**Características**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información descriptiva sobre las funcionalidades. Esta propiedad se hereda del [**elemento \_ CIMCapabilities.**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)



| Value                                                                                                                                                                                                                       | Significado                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Valor**</dt> <dt>predeterminado 2</dt> </dl> | Las funcionalidades asociadas representan las funcionalidades predeterminadas del elemento administrado.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Actual**</dt> <dt>3</dt> </dl> | Las funcionalidades asociadas representan las funcionalidades actuales del elemento administrado.<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")
</dt> </dl>

Referencia a una instancia de la clase [**\_ InstalledEthernetSwitchExtension de Msvm**](msvm-installedethernetswitchextension.md) que representa la extensión instalada. Esta propiedad se hereda del [**elemento \_ CIMCapabilities.**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 


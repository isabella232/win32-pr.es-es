---
description: Describe las restricciones en las propiedades de un objeto EnabledLogicalElement de CIM \_ asociado.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbec7b52d735b6dcff4da4c211da1db8b36d18adf20798fdcaa3932e1761119a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695915"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>Cim \_ EnabledLogicalElementCapabilities (clase)

Describe las restricciones en las propiedades de un objeto [**\_ EnabledLogicalElement de CIM**](cim-enabledlogicalelement.md) asociado.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Miembros

La **clase \_ ENABLEDLogicalElementCapabilities** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ENABLEDLogicalElementCapabilities** de CIM tiene estas propiedades.

<dl> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ UNIT CONFIG \_ \_ CAPS T \_ \| EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedElement**](cim-managedelement.md).**ElementName**")
</dt> </dl>

**True** si se puede modificar la propiedad **ElementName** del elemento lógico habilitado; de lo contrario, **false**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")
</dt> </dl>

Expresión regular que indica las restricciones en la **propiedad ElementName** del elemento lógico enable. Consulte *ABNF estándar dmtf con la guía de* uso de especificación de perfil de administración , apéndice C para obtener la sintaxis permitida.

> [!Note]  
> Si esta propiedad y **la propiedad ElementNameMask** del elemento lógico enable describen la longitud máxima de **ElementName**, se usa el valor más pequeño.

 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ UNIT CONFIG \_ \_ CAPS T \_ \| MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ FCSwitchCapabilities.ElementNameEditSupported", "**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")
</dt> </dl>

Longitud máxima admitida de la **propiedad ElementName** del elemento lógico habilitado.

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")
</dt> </dl>

Los posibles estados que el método [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) puede solicitar en el elemento lógico habilitado.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Apagar** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Sin** conexión (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Prueba** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Aplazar** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Quiesce** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Reinicio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Restablecer** (11)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Funcionalidades de CIM \_**](cim-capabilities.md)
</dt> </dl>

 


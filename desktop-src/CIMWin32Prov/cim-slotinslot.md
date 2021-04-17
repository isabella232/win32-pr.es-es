---
description: La \_ relación SlotInSlot de CIM representa la capacidad de un adaptador especial de extender la estructura de ranura existente para habilitar la conexión de tarjetas que, de lo contrario, no es compatible con un marco o un panel de hospedaje.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659372"
---
# <a name="cim_slotinslot-class"></a>\_Clase SlotInSlot de CIM

La **relación \_ SlotInSlot de CIM** representa la capacidad de un adaptador especial de extender la estructura de ranura existente para habilitar la conexión de tarjetas que, de lo contrario, no es compatible con un marco o un panel de hospedaje. Las ranuras son tipos especiales de conectores en los que normalmente se insertan tarjetas adaptadoras. El adaptador crea eficazmente una nueva ranura y se puede considerar (conceptualmente) como una ranura en una ranura. Las tarjetas que de otro modo serían físicamente o eléctricamente incompatibles con las ranuras existentes se admitirían al interactuar con la ranura proporcionada por el adaptador. Por ejemplo, las tarjetas de red son muy costosas. A medida que el nuevo hardware está disponible, cambian las configuraciones de chasis y tarjeta. Para proteger la inversión de sus clientes, los proveedores de redes fabrican adaptadores especiales que permiten que las tarjetas antiguas se ajusten a nuevos chasis o paneles de hospedaje o a tarjetas nuevas para caber en tarjetas antiguas mediante el uso de un adaptador especial que se adapta a una o más ranuras existentes y presenta una nueva ranura en la que puede caber la tarjeta.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ SlotInSlot** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SlotInSlot** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ranura CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Una [**\_ ranura CIM**](cim-slot.md) que describe las ranuras existentes de la placa de hospedaje o fotograma que se está adaptando para dar cabida a una tarjeta que de otro modo no sería físicamente o eléctricamente compatible con ella.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ranura CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Una [**\_ ranura CIM**](cim-slot.md) que describe la nueva ranura proporcionada por la placa del adaptador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ SlotInSlot** se deriva de [**CIM \_ ConnectTo**](cim-connectedto.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Connected de CIM**](cim-connectedto.md)
</dt> </dl>

 


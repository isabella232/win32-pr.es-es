---
description: La relación slotInSlot de CIM representa la capacidad de un adaptador especial de extender la estructura de ranura existente para permitir que las tarjetas incompatibles de otro modo se conecten a un marco o placa \_ de hospedaje.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: CIM_SlotInSlot clase
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
ms.openlocfilehash: 8163fbad7d517c936e764b51f91c77c821a33e05a6c4bdd3226246c9a27ce7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919375"
---
# <a name="cim_slotinslot-class"></a>Cim \_ SlotInSlot (clase)

La **relación \_ slotInSlot** de CIM representa la capacidad de un adaptador especial de extender la estructura de ranura existente para permitir que las tarjetas incompatibles de otro modo se conecten a un marco o placa de hospedaje. Las ranuras son tipos especiales de conectores en los que normalmente se insertan tarjetas de adaptador. El adaptador crea eficazmente una nueva ranura y se puede pensar (conceptualmente) como una ranura en una ranura. Las tarjetas que, de lo contrario, no serían compatibles física o eléctricamente con las ranuras existentes, se admiten mediante la interacción con la ranura proporcionada por el adaptador. Por ejemplo, los paneles de red son muy caros. A medida que el nuevo hardware está disponible, cambian las configuraciones de chasis y tarjeta. Para proteger la inversión de sus clientes, los proveedores de redes fabricarán adaptadores especiales que permiten que las tarjetas antiguas quepa en nuevos chasis o paneles de hospedaje o tarjetas nuevas para ajustarse a tarjetas antiguas mediante un adaptador especial que se ajuste a una o varias ranuras existentes y presente una nueva ranura en la que la tarjeta puede caber.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

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

La **clase \_ SlotInSlot** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SlotInSlot** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Ranura CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Una [**\_ ranura CIM**](cim-slot.md) que describe las ranuras existentes del tablero de hospedaje o el marco que se están adaptando para dar cabida a una tarjeta que, de lo contrario, no sería compatible física o eléctricamente con ella.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Ranura CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Una [**ranura CIM \_**](cim-slot.md) que describe la nueva ranura proporcionada por la placa adaptadora.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SlotInSlot** de CIM se deriva de [**CIM \_ ConnectedTo**](cim-connectedto.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> </dl>

 


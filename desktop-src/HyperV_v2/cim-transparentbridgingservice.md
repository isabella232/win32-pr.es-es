---
description: Representa el aspecto de puente transparente de un \_ objeto SwitchService de CIM.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8744bbac256d0cebc6d340ac83c4e8da746c03b298e2e3cd6c542310b3fc4914
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254985"
---
# <a name="cim_transparentbridgingservice-class"></a>\_Cim TransparentBridgingService (clase)

Representa el aspecto de puente transparente de un [**\_ objeto SwitchService**](cim-switchservice.md) de CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a>Miembros

La **clase \_ TransparentBridgingService** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ TransparentBridgingService** de CIM tiene estas propiedades.

<dl> <dt>

**AgingTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| BRIDGE-MIB.dot1dTpAgingTime")
</dt> </dl>

Período de tiempo de espera, en segundos, para agotar la información de reenvío aprendida dinámicamente. El estándar 802.1D-1990 recomienda un valor predeterminado de 300 segundos.

</dd> <dt>

**Fid**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de base de datos de filtrado que usan los conmutadores con vlan que tienen más de una base de datos de filtrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ForwardingService**](cim-forwardingservice.md)
</dt> </dl>

 


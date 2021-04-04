---
description: Representa el aspecto de puente transparente de un \_ objeto SwitchService de CIM.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: CIM_TransparentBridgingService (clase)
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
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908730"
---
# <a name="cim_transparentbridgingservice-class"></a>\_Clase TransparentBridgingService de CIM

Representa el aspecto de puente transparente de un objeto [**\_ SwitchService de CIM**](cim-switchservice.md) .

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

La clase **CIM \_ TransparentBridgingService** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ TransparentBridgingService** tiene estas propiedades.

<dl> <dt>

**AgingTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpAgingTime ")
</dt> </dl>

Período de tiempo de espera, en segundos, durante el que se va a obtener la información de reenvío obtenida dinámicamente. El estándar 802.1 D-1990 recomienda un valor predeterminado de 300 segundos.

</dd> <dt>

**FID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Filtrado de identificador de base de datos utilizado por conmutadores compatibles con VLAN que tienen más de una base de datos de filtrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_FORWARDINGSERVICE CIM**](cim-forwardingservice.md)
</dt> </dl>

 


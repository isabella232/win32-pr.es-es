---
description: Representa un puerto de conmutador que envía y recibe tramas de datos.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: CIM_SwitchPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002016"
---
# <a name="cim_switchport-class"></a>\_Clase de SWITCHPORT CIM

Representa un puerto de conmutador que envía y recibe tramas de datos.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a>Miembros

La clase de **\_ SwitchPort de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ SwitchPort de CIM** tiene estas propiedades.

<dl> <dt>

**NúmeroDePuerto**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dPort ")
</dt> </dl>

El identificador numérico del puerto del conmutador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ProtocolEndpoint de CIM \_**](cim-protocolendpoint.md)
</dt> </dl>

 


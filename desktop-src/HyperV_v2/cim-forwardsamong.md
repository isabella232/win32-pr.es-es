---
description: Representa una asociación en la que los extremos de protocolo dependen de un servicio de reenvío para reenviar los datos.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: CIM_ForwardsAmong (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686513"
---
# <a name="cim_forwardsamong-class"></a>\_Clase ForwardsAmong de CIM

Representa una asociación en la que los extremos de protocolo dependen de un servicio de reenvío para reenviar los datos.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ForwardsAmong** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ForwardsAmong** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ProtocolEndpoint de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Los extremos del protocolo envían y reciben los datos reenviados.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ForwardingService**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Servicio de reenvío que reenvía los datos.

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

[**\_SERVICESAPDEPENDENCY CIM**](cim-servicesapdependency.md)
</dt> </dl>

 


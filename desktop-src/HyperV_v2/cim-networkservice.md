---
description: Esta clase está en desuso. En su lugar, se recomienda derivar de la \_ clase de servicio CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688376"
---
# <a name="cim_networkservice-class"></a>Clase de NetworkService de CIM \_

Esta clase está en desuso. En su lugar, se recomienda derivar de la clase de [**\_ servicio CIM**](cim-service.md) .

## <a name="syntax"></a>Sintaxis

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a>Miembros

La clase de **\_ NetworkService de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ NetworkService de CIM** tiene estas propiedades.

<dl> <dt>

**Palabras clave**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

> [!Note]  
> Descripción desusada: una matriz de palabras clave que se pueden usar en las consultas.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Esta propiedad está desusada. En su lugar, se recomienda la clase **CIM \_ ServiceAccessURI** .

> [!Note]  
> Descripción desusada: una dirección URL que proporciona el protocolo, la ubicación de red y otra información específica del servicio necesaria para obtener acceso al servicio.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

> [!Note]  
> Descripción desusada: las condiciones previas que deben cumplirse para que este servicio se inicie correctamente.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

> [!Note]  
> Descripción desusada: los parámetros que se deben proporcionar al método **StartService** para que este servicio se inicie correctamente.

 

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

[**\_Servicio CIM**](cim-service.md)
</dt> </dl>

 


---
description: Esta clase está en desuso. En su lugar, se recomienda derivar de la clase de \_ servicio CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService clase
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
ms.openlocfilehash: cfb2ea7b122516cc3b62f675684649e22577171f713856638f97985d9713e8d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694695"
---
# <a name="cim_networkservice-class"></a>Clase \_ NetworkService de CIM

Esta clase está en desuso. En su lugar, se recomienda derivar de la clase [**de \_ servicio CIM.**](cim-service.md)

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

La **clase \_ NetworkService** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ NetworkService de CIM** tiene estas propiedades.

<dl> <dt>

**Palabras clave**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

> [!Note]  
> Descripción en desuso: matriz de palabras clave que se pueden usar en las consultas.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Esta propiedad está desusada. En su lugar, se recomienda la **\_ clase CIM ServiceAccessURI.**

> [!Note]  
> Descripción en desuso: dirección URL que proporciona el protocolo, la ubicación de red y otra información específica del servicio necesaria para acceder al servicio.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

> [!Note]  
> Descripción en desuso: las condiciones previas que se deben cumplir para que este servicio se inicie correctamente.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor")
</dt> </dl>

Esta propiedad está en desuso y no debe utilizarse.

> [!Note]  
> Descripción en desuso: parámetros que se deben proporcionar al **método StartService** para que este servicio se inicie correctamente.

 

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

[**Servicio \_ CIM**](cim-service.md)
</dt> </dl>

 


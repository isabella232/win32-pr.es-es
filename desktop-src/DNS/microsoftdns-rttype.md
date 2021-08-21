---
title: MicrosoftDNS_RTType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro Route Through (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType dns de clase
- MicrosoftDNS_RTType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287dc3d80370f812b6ee721b9556f906df289c67a17048aa326efc3b80de5954
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077065"
---
# <a name="microsoftdns_rttype-class"></a>MicrosoftDNS \_ RTType (clase)

Subclase de [**\_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro Route Through (RT).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a>Miembros

La **clase MicrosoftDNS \_ RTType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MicrosoftDNS \_ RTType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un tipo RT de RR en función de los datos de los parámetros de entrada del método: nombre del servidor DNS del registro, nombre de contenedor, nombre de propietario/host, clase (valor predeterminado = IN), valor de período de vida, preferencia de registro y nombre de host intermedio. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Actualiza el TTL, las preferencias y el host intermedio a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>        |



 

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ RTType** tiene estas propiedades.

<dl> <dt>

**IntermediateHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un host que sirve como intermedio para llegar al host especificado por el propietario.

</dd> <dt>

**Referencia**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Preferencia dada a este RR entre otros en el mismo propietario. Se prefieren valores más bajos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método CreateInstanceFromPropertyData de la clase MICROSOFTDNS \_ RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase RTType de MicrosoftDNS \_**](microsoftdns-rttype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






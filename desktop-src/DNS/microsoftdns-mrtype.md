---
title: MicrosoftDNS_MRType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de cambio de nombre de buzón (MR).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- DNS de la clase MicrosoftDNS_MRType
- MicrosoftDNS_MRType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 732f0e6f51963f5ae810e4730406a94264fdde47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150811"
---
# <a name="microsoftdns_mrtype-class"></a>MicrosoftDNS ( \_ clase MRType)

La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de cambio de nombre de buzón (MR).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ MRType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ MRType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Este método crea una instancia de un tipo ' MR ' de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del buzón, la clase (valor predeterminado = IN), el valor de período de vida y el cambio de nombre del buzón. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Este método actualiza el TTL y el buzón MR a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>                 |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ MRType** tiene estas propiedades.

<dl> <dt>

**MRMailbox**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un buzón que es el cambio de nombre adecuado del buzón especificado en el nombre del propietario del registro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MRType**](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS MRType**](microsoftdns-mrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






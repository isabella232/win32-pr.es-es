---
title: MicrosoftDNS_MBType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de recursos de buzón (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- DNS de la clase MicrosoftDNS_MBType
- MicrosoftDNS_MBType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ad6599ad058f65beba961f00c1bd6c43663487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996549"
---
# <a name="microsoftdns_mbtype-class"></a>MicrosoftDNS ( \_ clase MBType)

La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de recursos de buzón (MB).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ MBType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ MBType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un RR de MB en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del buzón, la clase (valor predeterminado = IN), el valor de período de vida y el host de buzón. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Actualiza el host de TTL y MB a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>        |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ MBType** tiene estas propiedades.

<dl> <dt>

**MBHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un host del buzón especificado en el nombre del propietario del registro.

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

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MBType**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS MBType**](microsoftdns-mbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






---
title: MicrosoftDNS_AType (clase)
description: Subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de dirección de host (a).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- DNS de la clase MicrosoftDNS_AType
- MicrosoftDNS_AType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType
- MicrosoftDNS_AType.CreateInstanceFromPropertyData
- MicrosoftDNS_AType.Modify
- MicrosoftDNS_AType.IPAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e856968e2c3d4e581d69e0ac7bcbddc256424c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656537"
---
# <a name="microsoftdns_atype-class"></a>MicrosoftDNS ( \_ clase AType)

Subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de dirección de host (a).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ AType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ AType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un RR de dirección de host (A) basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la dirección IP del host. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Actualiza el TTL y la dirección IP a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>             |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ AType** tiene estas propiedades.

<dl> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que representa la dirección IPv4 del host.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AType**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS AType**](microsoftdns-atype-modify.md)
</dt> </dl>

 

 






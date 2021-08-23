---
title: MicrosoftDNS_AType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro de dirección de host (A).
ms.assetid: c7bd8a26-b0ac-49ef-9068-a0ecddeb6ef4
keywords:
- MicrosoftDNS_AType DNS de clase
- MicrosoftDNS_AType clase DNS , descrita
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
ms.openlocfilehash: 4fb5cd5735d30d4b512c2dd382f6ef59b182da51c99df26ccebddbdc0e2a1837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574095"
---
# <a name="microsoftdns_atype-class"></a>Clase MicrosoftDNS \_ AType

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de dirección de host (A).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_AType : MicrosoftDNS_ResourceRecord
{
  string IPAddress;
};
```

## <a name="members"></a>Miembros

La **clase MicrosoftDNS \_ AType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MicrosoftDNS \_ AType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un RR de dirección de host (A) en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la dirección IP del host. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Implementado, estático<br/> |
| **Modificar**                         | Actualiza el TTL y la dirección IP a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>             |



 

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ AType** tiene estas propiedades.

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
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Método CreateInstanceFromPropertyData de la clase MicrosoftDNS \_ AType**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase MicrosoftDNS \_ AType**](microsoftdns-atype-modify.md)
</dt> </dl>

 

 






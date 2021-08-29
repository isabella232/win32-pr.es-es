---
title: MicrosoftDNS_ATMAType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro ATMA (Dirección a nombre de ATM).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- MicrosoftDNS_ATMAType dns de clase
- MicrosoftDNS_ATMAType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 441fdfb8e07ad7206d21a1979381089cf03bfa875251f084eddbd45fba0f4e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795655"
---
# <a name="microsoftdns_atmatype-class"></a>MicrosoftDNS \_ ATMAType (clase)

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro ATMA (Dirección a nombre de ATM).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a>Miembros

La **clase \_ ATMAType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MICROSOFTDNS \_ ATMAType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un registro de recursos ATMA en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario o nodo, la clase (valor predeterminado = IN), el valor de período de vida y el formato y la dirección de ATM. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Actualiza TTL, Format y ATMA Address a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>         |



 

### <a name="properties"></a>Propiedades

La **clase MICROSOFTDNS \_ ATMAType** tiene estas propiedades.

<dl> <dt>

**ATMAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de longitud variable de octetos que contiene la dirección ATM del nodo o propietario al que pertenece este RR. Los primeros 4 bytes de la matriz se usan para almacenar el tamaño de la cadena de octeto. El byte más significativo se almacena en byte 0.

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Formato de dirección DE ATM. Los valores válidos son: 0 que indica el formato de dirección del sistema de finalización de ATM (AESA) y 1 que indica el formato E.164.

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

[**Método CreateInstanceFromPropertyData de la clase \_ ATMAType de MicrosoftDNS**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase ATMAType de MicrosoftDNS \_**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






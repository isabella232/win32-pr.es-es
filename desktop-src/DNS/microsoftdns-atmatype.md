---
title: MicrosoftDNS_ATMAType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de dirección ATM a nombre (Atma).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS de la clase MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType de la clase DNS, descrito
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
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996398"
---
# <a name="microsoftdns_atmatype-class"></a>MicrosoftDNS ( \_ clase ATMAType)

La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de dirección ATM a nombre (Atma).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ ATMAType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ ATMAType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un registro de recursos ATMA en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el propietario o el nombre del nodo, la clase (valor predeterminado = IN), el valor de período de vida y el formato y la dirección ATM. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Actualiza el TTL, el formato y la dirección ATMA a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>         |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ ATMAType** tiene estas propiedades.

<dl> <dt>

**ATMAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de longitud variable de octetos que contiene la dirección ATM del nodo/propietario al que pertenece este RR. Los primeros 4 bytes de la matriz se utilizan para almacenar el tamaño de la cadena de octeto. El byte más significativo se almacena en byte 0.

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Formato de dirección ATM. Los valores válidos son: 0 indica el formato de dirección del sistema de finalización (AESA) de ATM y 1 indica el formato E. 164.

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

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS ATMAType**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






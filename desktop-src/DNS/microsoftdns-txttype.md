---
title: MicrosoftDNS_TXTType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de texto (txt).
ms.assetid: e4bd445f-71c4-48dc-b210-e3ad4452d2e5
keywords:
- DNS de la clase MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_TXTType.Modify
- MicrosoftDNS_TXTType.DescriptiveText
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d89563240b8e6d6bedb51cbe802180cd7577b57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658349"
---
# <a name="microsoftdns_txttype-class"></a>MicrosoftDNS ( \_ clase TXTType)

La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de texto (txt).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_TXTType : MicrosoftDNS_ResourceRecord
{
  string DescriptiveText;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ TXTType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ TXTType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un tipo TXT de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el texto del registro. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/>        |
| **Modify**                         | Actualiza el TTL y el texto descriptivo a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/> |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ TXTType** tiene estas propiedades.

<dl> <dt>

**DescriptiveText**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Texto descriptivo, la semántica de que depende del dominio del propietario.

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

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS TXTType**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS TXTType**](microsoftdns-txttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






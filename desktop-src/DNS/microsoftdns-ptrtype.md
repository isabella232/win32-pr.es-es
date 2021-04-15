---
title: MicrosoftDNS_PTRType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de puntero (PTR).
ms.assetid: 2cb0f13b-e683-473b-9cdd-bc5d805b919d
keywords:
- DNS de la clase MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType
- MicrosoftDNS_PTRType.CreateInstanceFromPropertyData
- MicrosoftDNS_PTRType.Modify
- MicrosoftDNS_PTRType.PTRDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65dc434eb751ed925ab9efcdaf29f04741b749ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534336"
---
# <a name="microsoftdns_ptrtype-class"></a>MicrosoftDNS ( \_ clase PTRType)

La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de puntero (PTR).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_PTRType : MicrosoftDNS_ResourceRecord
{
  string PTRDomainName;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ PTRType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ PTRType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un registro de recursos de DNS PTR en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el FQDN del registro PTR. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Actualiza el nombre de dominio TTL y PTR a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>                 |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ PTRType** tiene estas propiedades.

<dl> <dt>

**PTRDomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN de los datos del registro PTR.

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

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS PTRType**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS PTRType**](microsoftdns-ptrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






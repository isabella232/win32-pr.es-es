---
title: MicrosoftDNS_MGType (clase)
description: La subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de grupo de correo (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- DNS de la clase MicrosoftDNS_MGType
- MicrosoftDNS_MGType de la clase DNS, descrito
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535356"
---
# <a name="microsoftdns_mgtype-class"></a>MicrosoftDNS ( \_ clase MGType)

La subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de grupo de correo (mg).

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ MGType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ MGType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Este método crea una instancia de un tipo MG de RR basándose en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del grupo de correo, la clase (valor predeterminado = IN), el valor de período de vida y el nombre del buzón. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Este método actualiza el buzón TTL y MG a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>                |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ MGType** tiene estas propiedades.

<dl> <dt>

**MGMailbox**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un buzón que es miembro del grupo de correo especificado por el nombre del propietario del registro.

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

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS MGType**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS MGType**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






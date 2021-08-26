---
title: MicrosoftDNS_ISDNType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro ISDN.
ms.assetid: 8925042c-65d3-465f-aedd-9f7c862620b5
keywords:
- MicrosoftDNS_ISDNType dns de clase
- MicrosoftDNS_ISDNType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType
- MicrosoftDNS_ISDNType.CreateInstanceFromPropertyData
- MicrosoftDNS_ISDNType.Modify
- MicrosoftDNS_ISDNType.ISDNNumber
- MicrosoftDNS_ISDNType.SubAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af06ad782b6d36213e9a1df210916f9346e1e4f8bd0a98dd619651a579dc5c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131725"
---
# <a name="microsoftdns_isdntype-class"></a>Clase ISDNType de MicrosoftDNS \_

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro ISDN.

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_ISDNType : MicrosoftDNS_ResourceRecord
{
  string ISDNNumber;
  string SubAddress;
};
```

## <a name="members"></a>Miembros

La **clase MicrosoftDNS \_ ISDNType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ISDNType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un registro de recursos isdn en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y el número y la subdirección isdn del propietario. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Actualiza el TTL, el número ISDN y la subdirección a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>                   |



 

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ ISDNType** tiene estas propiedades.

<dl> <dt>

**ISDNNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número ISDN y DDI del propietario del registro.

</dd> <dt>

**Subdirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Subdirección del propietario, si se define.

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

[**Método CreateInstanceFromPropertyData de la clase \_ ISDNType de MicrosoftDNS**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase \_ ISDNType de MicrosoftDNS**](microsoftdns-isdntype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






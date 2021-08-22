---
title: MicrosoftDNS_AAAAType clase
description: Subclase de ResourceRecord de MicrosoftDNS que representa un registro de dirección \_ IPv6 (AAAA). El registro AAAA se pronuncia normalmente \ 0034;registro de cuatro a \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType dns de clase
- MicrosoftDNS_AAAAType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90628ba4ceedffe9628aca0b96b624377ae7a8ab2351cfe6ae6b43ba8a381235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587575"
---
# <a name="microsoftdns_aaaatype-class"></a>Clase AAAAType de MicrosoftDNS \_

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de dirección IPv6 (AAAA). El registro AAAA se pronuncia normalmente como "registro de cuatro a".

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a>Miembros

La **clase \_ AAAAType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ AAAAType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un tipo "AAAA" de RR en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre de propietario/host, la clase (valor predeterminado = IN), el valor de período de vida y la dirección IPv6. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Implementado, estático<br/> |
| **Modificar**                         | Actualiza la dirección TTL e IPv6 a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>      |



 

### <a name="properties"></a>Propiedades

La **clase \_ AAAAType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**IPv6Address**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección IPv6 del host.

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

[**Método CreateInstanceFromPropertyData de la clase AAAAType de MicrosoftDNS \_**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase \_ AAAAType de MicrosoftDNS**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






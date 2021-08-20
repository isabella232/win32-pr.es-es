---
title: MicrosoftDNS_WINSType clase
description: Subclase de ResourceRecord de MicrosoftDNS que representa un Windows servicio de nombres \_ de Internet (WINS).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- MicrosoftDNS_WINSType DNS de clase
- MicrosoftDNS_WINSType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089faa6fa3cda6780b600dbf6c296fd1ce71f902428e6c2abe16f92dada1e219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162845"
---
# <a name="microsoftdns_winstype-class"></a>Clase WINSType de MicrosoftDNS \_

Subclase de [**\_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un Windows servicio de nombres de Internet (WINS).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a>Miembros

La **clase \_ WINSType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ WINSType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un tipo WINS de RR en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación WINS, el tiempo de espera de búsqueda, el tiempo de espera de caché y la lista de direcciones IP para la búsqueda. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Implementado, estático<br/> |
| **Modificar**                         | Actualiza los servidores TTL, Mapping Flag, Look-up Time Out, Cache Time Out y Wins a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>                      |



 

### <a name="properties"></a>Propiedades

La **clase \_ WINSType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, que un servidor DNS que usa WINS Look up puede almacenar en caché la respuesta del servidor WINS.

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tiempo, en segundos, que un servidor DNS intenta resolver mediante WINS Look up.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de asignación WINS que especifica si el registro debe incluirse en la replicación de zona. Puede tener solo dos valores: 0x80000000 y 0x00010000 correspondientes a las marcas de replicación y sin replicación (registro local), respectivamente. Los valores siguientes son válidos.



| Value                                                                                                                                               | Significado                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Marca de replicación<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Marca De no replicación (registro local)<br/> |



 

</dd> <dt>

**WinsServers**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de direcciones IP separadas por comas de servidores WINS que se usan en búsquedas WINS.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método CreateInstanceFromPropertyData de la clase WINSType de MicrosoftDNS \_**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase WINSType de MicrosoftDNS \_**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






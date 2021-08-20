---
title: MicrosoftDNS_HINFOType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro de información de host (HINFO).
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- MicrosoftDNS_HINFOType dns de clase
- MicrosoftDNS_HINFOType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95aa97307342a36e6fd8e3746cb975b0f9e579d0ad7fe76b40c34a429f777c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163297"
---
# <a name="microsoftdns_hinfotype-class"></a>Clase MicrosoftDNS \_ HINFOType

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de información de host (HINFO).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a>Miembros

La **clase MicrosoftDNS \_ HINFOType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MicrosoftDNS \_ HINFOType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un HINFO de RR en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario, la clase (valor predeterminado = IN), el valor de período de vida y los tipos de cpu y sistema operativo del host. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Actualiza el TTL, la CPU y el sistema operativo a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>          |



 

### <a name="properties"></a>Propiedades

La **clase MicrosoftDNS \_ HINFOType** tiene estas propiedades.

<dl> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de CPU del propietario del registro.

</dd> <dt>

**SISTEMA OPERATIVO**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Sistema operativo del propietario del registro.

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

[**Método CreateInstanceFromPropertyData de la clase MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






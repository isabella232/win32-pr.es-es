---
title: MicrosoftDNS_NXTType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un RR siguiente (NXT).
ms.assetid: bb24509e-083b-4432-89e3-501167f12299
keywords:
- MicrosoftDNS_NXTType dns de clase
- MicrosoftDNS_NXTType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
- MicrosoftDNS_NXTType.Modify
- MicrosoftDNS_NXTType.NextDomainName
- MicrosoftDNS_NXTType.Types
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36fa67d3d1ab60aa4af6c0be7269f068edaf42a64fa9cf1cfea68ca23d82ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913105"
---
# <a name="microsoftdns_nxttype-class"></a>Clase NXTType de MicrosoftDNS \_

Subclase [**de \_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un RR siguiente (NXT).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_NXTType : MicrosoftDNS_ResourceRecord
{
  string NextDomainName;
  string Types;
};
```

## <a name="members"></a>Miembros

La **clase \_ NXTType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ NXTType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un registro de recursos NXT en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre de propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación WINS, el tiempo de espera de búsqueda inversa, el tiempo de espera de la caché WINS y el nombre de dominio que se va a anexar. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Implementado, estático<br/>                                                                                                                                           |
| **Modificar**                         | Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de caché y el dominio de resultados a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/> **Windows Server 2003:** Este método también actualiza NextDomainName y Types a los valores especificados como parámetros de entrada de este método.<br/> <br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ NXTType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**NextDomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Siguiente nombre de dominio.

</dd> <dt>

**Tipos**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista separada por espacios de los elementos mnemotécnicos de tipo RR para el nombre de propietario del registro de recursos NXT.

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

[**Método CreateInstanceFromPropertyData de la clase NXTType de MicrosoftDNS \_**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase NXTType de MicrosoftDNS \_**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






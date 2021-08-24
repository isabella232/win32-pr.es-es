---
title: MicrosoftDNS_AFSDBType clase
description: Subclase de ResourceRecord de MicrosoftDNS que representa un registro del servidor de base de datos del sistema de archivos \_ Andrew (AFSDB).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType dns de clase
- MicrosoftDNS_AFSDBType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7887d51e58b8c34374ed5ca96d0206472155872ba573b7b9f8879329910f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815705"
---
# <a name="microsoftdns_afsdbtype-class"></a>Clase AFSDBType de MicrosoftDNS \_

Subclase [**de \_ ResourceRecord de MicrosoftDNS que**](microsoftdns-resourcerecord.md) representa un registro del servidor de base de datos del sistema de archivos Andrew (AFSDB).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Miembros

La **clase \_ AFSDBType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ AFSDBType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un registro de recursos de AFSDB en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario o la celda, la clase (valor predeterminado = IN), el valor de período de vida y el subtipo y el nombre del servidor AFS del host. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Este método actualiza el TTL, el subtipo y el nombre del servidor a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>   |



 

### <a name="properties"></a>Propiedades

La **clase \_ AFSDBType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un host que tiene un servidor para la celda afs especificada en el nombre de propietario.

</dd> <dt>

**Subtipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Subtipo del servidor afs host. Para el subtipo 1 (valor =1), el host tiene un servidor de ubicación de volumen afs versión 3.0 para la celda afs con nombre. En el caso del subtipo 2 (valor=2), el host tiene un servidor de nombres autenticado que contiene el nodo de directorio raíz de celda para la celda DCE/NCA con nombre.

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

[**Método CreateInstanceFromPropertyData de la clase \_ AFSDBType de MicrosoftDNS**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase \_ AFSDBType de MicrosoftDNS**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






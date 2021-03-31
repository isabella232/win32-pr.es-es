---
title: MicrosoftDNS_AFSDBType (clase)
description: Subclase de MicrosoftDNS \_ ResourceRecord que representa un registro de servidor de base de datos del sistema de archivos (AFSDB) Andrew.
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- DNS de la clase MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType de la clase DNS, descrito
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
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079388"
---
# <a name="microsoftdns_afsdbtype-class"></a>MicrosoftDNS ( \_ clase AFSDBType)

Subclase de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) que representa un registro de servidor de base de datos del sistema de archivos (AFSDB) Andrew.

La siguiente sintaxis se simplifica desde el código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Miembros

La clase **MicrosoftDNS \_ AFSDBType** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MicrosoftDNS \_ AFSDBType** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea una instancia de un registro de recursos AFSDB basado en los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario o la celda, la clase (valor predeterminado = IN), el valor de período de vida y el subtipo y nombre del servidor AFS del host. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modify**                         | Este método actualiza el TTL, el subtipo y el nombre del servidor a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: implementados<br/>   |



 

### <a name="properties"></a>Propiedades

La clase **MicrosoftDNS \_ AFSDBType** tiene estas propiedades.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un host que tiene un servidor para la celda AFS especificada en el nombre del propietario.

</dd> <dt>

**Subtype**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Subtipo del servidor AFS del host. Para el subtipo 1 (valor = 1), el host tiene un servidor de ubicación del volumen AFS versión 3,0 para la celda AFS con nombre. En el caso del subtipo 2 (valor = 2), el host tiene un servidor de nombres autenticado que contiene el nodo del directorio raíz de la celda para la celda de DCE/NCA con nombre.

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

[**Método CreateInstanceFromPropertyData de la \_ clase MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la \_ clase MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






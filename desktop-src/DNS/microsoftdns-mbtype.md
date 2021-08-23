---
title: MicrosoftDNS_MBType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro de recursos de buzón de correo (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- MicrosoftDNS_MBType dns de clase
- MicrosoftDNS_MBType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccea0cc9c30fb8a46debedaa2aeb0811ed63b08005919c7f189d771fd7daed2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163270"
---
# <a name="microsoftdns_mbtype-class"></a>Clase MBType de MicrosoftDNS \_

Subclase de [**\_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de recursos de buzón de correo (MB).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a>Miembros

La **clase \_ MBType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ MBType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un RR de MB en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre de propietario del buzón, la clase (valor predeterminado = IN), el valor de período de vida y el host de buzón de correo. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/> |
| **Modificar**                         | Actualiza el host TTL y MB a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>        |



 

### <a name="properties"></a>Propiedades

La **clase \_ MBType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**MBHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un host del buzón especificado en el nombre de propietario del registro.

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

[**Método CreateInstanceFromPropertyData de la clase MBType de MicrosoftDNS \_**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase MBType de MicrosoftDNS \_**](microsoftdns-mbtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






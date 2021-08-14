---
title: MicrosoftDNS_MGType clase
description: Subclase de ResourceRecord de MicrosoftDNS \_ que representa un registro de grupo de correo (MG).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType DNS de clase
- MicrosoftDNS_MGType clase DNS , descrita
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
ms.openlocfilehash: af4a9b1f88a3d7e2752d2e4c199c261b49364ab7bdcbf4543e852f5218111491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692605"
---
# <a name="microsoftdns_mgtype-class"></a>Clase MGType de MicrosoftDNS \_

Subclase de [**\_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de grupo de correo (MG).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a>Miembros

La **clase \_ MGType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ MGType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Este método crea una instancia de un tipo MG de RR en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre del propietario del grupo de correo, la clase (valor predeterminado = IN), el valor de período de vida y el nombre del buzón. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: Implementado, estático<br/> |
| **Modificar**                         | Este método actualiza el buzón de TTL y MG a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/>                |



 

### <a name="properties"></a>Propiedades

La **clase \_ MGType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**MGMailbox**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

FQDN que especifica un buzón que es miembro del grupo de correo especificado por el nombre de propietario del registro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Método CreateInstanceFromPropertyData de la clase MGType de MicrosoftDNS \_**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase MGType de MicrosoftDNS \_**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 






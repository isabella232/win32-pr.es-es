---
description: Proporciona propiedades y métodos que puede usar para elegir, administrar y usar almacenes de certificados y los certificados de esos almacenes.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Almacenar objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1de500d10d6bd5493492b62a2abb618be3cdb19d48a89beaf7ab83d55a86ac28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972302"
---
# <a name="store-object"></a>Almacenar objeto

\[El **objeto Store** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto Store** proporciona propiedades y métodos que puede [](../secgloss/c-gly.md) usar para elegir, administrar y usar almacenes de certificados y los certificados de esos almacenes. CAPICOM puede usar current-user, local-machine, memoria y Active Directory almacenes. Además, los almacenes admiten almacenes de certificados basados en tarjetas inteligentes. Los desarrolladores deben tener en cuenta que algunos métodos pueden producir errores con algunos almacenes si se intentan realizar operaciones para las que el usuario no tiene derechos.

## <a name="members"></a>Miembros

El **objeto Store** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Store** tiene estos métodos.



| Método                         | Descripción                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Añadir**](store-add.md)       | Agrega un [**objeto Certificate**](certificate.md) al almacén de certificados abierto.<br/>                                                                                                                       |
| [**Cerrar**](store-close.md)   | Cierra un almacén de certificados abierto.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No se admite el método [**Close.**](store-close.md)<br/>                                                               |
| [**Eliminar**](store-delete.md) | Elimina el almacén de certificados representado por el objeto [**Store**](certificate.md) actual.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No [**se admite**](store-delete.md) el método Delete.<br/> |
| [**exportar**](store-export.md) | Exporta el almacén de un [*BLOB codificado.*](../secgloss/b-gly.md)<br/>                                                                                                       |
| [**Importar**](store-import.md) | Importa un almacén exportado previamente.<br/>                                                                                                                                                                  |
| [**Cargar**](store-load.md)     | Importa [**objetos**](certificate.md) Certificate de un archivo en el almacén.<br/>                                                                                                                        |
| [**Abierto**](store-open.md)     | Abre un almacén de certificados.<br/>                                                                                                                                                                            |
| [**Quitar**](store-remove.md) | Quita un [**objeto Certificate**](certificate.md) de un almacén abierto.<br/>                                                                                                                               |



 

### <a name="properties"></a>Propiedades

El **objeto Store** tiene estas propiedades.



| Propiedad                                              | Tipo de acceso          | Descripción                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](store-certificates.md)<br/> | Solo lectura<br/> | Recupera la [**colección Certificates**](certificates.md) del almacén. Esta es la propiedad predeterminada.<br/>                                                                                  |
| [**Ubicación**](store-location.md)<br/>         | Solo lectura<br/> | Recupera la ubicación del almacén de certificados que representa este objeto.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No [**se admite**](store-location.md) la propiedad Location.<br/> |
| [**Nombre**](store-name.md)<br/>                 | Solo lectura<br/> | Recupera el nombre del almacén de certificados que representa este objeto.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No [**se admite**](store-name.md) la propiedad Name.<br/>             |



 

## <a name="remarks"></a>Comentarios

Se **puede crear** el objeto Store y es seguro para el scripting. El ProgID del **objeto Store** es CAPICOM. Store.2.

**CAPICOM 1. *x:*** el ProgID del **objeto Store** es CAPICOM. Store.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 

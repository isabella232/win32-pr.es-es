---
description: Proporciona propiedades y métodos que puede usar para elegir, administrar y usar almacenes de certificados y certificados en esos almacenes.
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: Objeto Store
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
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649945"
---
# <a name="store-object"></a>Objeto Store

\[El objeto de **almacenamiento** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto de **almacén** proporciona propiedades y métodos que puede usar para elegir, administrar y usar [*almacenes de certificados*](../secgloss/c-gly.md) y los certificados de esas tiendas. CAPICOM puede utilizar el usuario actual, el equipo local, la memoria y los almacenes de Active Directory. Además, los almacenes admiten almacenes de certificados basados en tarjetas inteligentes. Los desarrolladores deben tener en cuenta que pueden producirse errores en algunos métodos con algunos almacenes si se intentan realizar operaciones para las que el usuario no tiene derechos.

## <a name="members"></a>Miembros

El objeto **Store** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **Store** tiene estos métodos.



| Método                         | Descripción                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Agréguela**](store-add.md)       | Agrega un objeto de [**certificado**](certificate.md) al almacén de certificados abierto.<br/>                                                                                                                       |
| [**Cercanos**](store-close.md)   | Cierra un almacén de certificados abierto.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No se admite el método [**Close**](store-close.md) .<br/>                                                               |
| [**Elimínelos**](store-delete.md) | Elimina el almacén de certificados representado por el objeto de [**almacén**](certificate.md) actual.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No se admite el método [**Delete**](store-delete.md) .<br/> |
| [**Exportación**](store-export.md) | Exporta el almacén de un [*BLOB*](../secgloss/b-gly.md)codificado.<br/>                                                                                                       |
| [**Importar**](store-import.md) | Importa un almacén exportado previamente.<br/>                                                                                                                                                                  |
| [**Cargar**](store-load.md)     | Importa los objetos de [**certificado**](certificate.md) de un archivo en el almacén.<br/>                                                                                                                        |
| [**Ábra**](store-open.md)     | Abre un almacén de certificados.<br/>                                                                                                                                                                            |
| [**Retirar**](store-remove.md) | Quita un objeto de [**certificado**](certificate.md) de un almacén abierto.<br/>                                                                                                                               |



 

### <a name="properties"></a>Propiedades

El objeto **Store** tiene estas propiedades.



| Propiedad                                              | Tipo de acceso          | Descripción                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](store-certificates.md)<br/> | Solo lectura<br/> | Recupera la colección de [**certificados**](certificates.md) del almacén. Esta es la propiedad predeterminada.<br/>                                                                                  |
| [**Location**](store-location.md)<br/>         | Solo lectura<br/> | Recupera la ubicación del almacén de certificados que este objeto representa.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No se admite la propiedad [**Location**](store-location.md) .<br/> |
| [**Name**](store-name.md)<br/>                 | Solo lectura<br/> | Recupera el nombre del almacén de certificados que este objeto representa.<br/> **CAPICOM 2.0.0.3 y versiones anteriores:** No se admite la propiedad [**Name**](store-name.md) .<br/>             |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto de **almacén** y es seguro para el scripting. El ProgID del objeto **Store** es CAPICOM. Almacén. 2.

**CAPICOM 1. *x*:** el identificador de programa (ProgID) del objeto **Store** es CAPICOM. Almacén. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 

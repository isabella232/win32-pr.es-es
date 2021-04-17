---
description: Representa una colección de objetos de certificado.
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: Objeto Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670303"
---
# <a name="certificates-object"></a>Objeto Certificates

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto de **certificados** representa una colección de objetos de [**certificado**](certificate.md) . Cada objeto de [**certificado**](certificate.md) representa un único [*certificado digital*](../secgloss/d-gly.md).

El objeto **Certificates** expone las siguientes interfaces:

-   **ICertificates2**: introducido en CAPICOM 2,0.
-   **ICertificates**: introducido en CAPICOM 1,0.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **certificados** se usa para realizar las siguientes tareas:

-   Agregue o quite un objeto de [**certificado**](certificate.md) de o de la colección.
-   Genere un subconjunto de la colección buscando un conjunto de certificados o mostrando un cuadro de diálogo para seleccionar los certificados.
-   Borre todos los objetos de [**certificado**](certificate.md) de la colección.
-   Recupere el número de certificados de la colección.
-   Recupera un objeto de [**certificado**](certificate.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto de **certificados** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **certificados** tiene estos métodos.



| Método                                | Descripción                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Agréguela**](certificates-add.md)       | Agrega un objeto de [**certificado**](certificate.md) a la colección.<br/> (Se hereda de **CertificatesICertificates2**)                                        |
| [**Claridad**](certificates-clear.md)   | Quita todos los objetos de [**certificado**](certificate.md) de la colección.<br/> (Se hereda de **CertificatesICertificates2**)                                |
| [**Buscar**](certificates-find.md)     | Devuelve un objeto de **certificados** que contiene todos los certificados que coinciden con los criterios de búsqueda especificados.<br/> (Se hereda de **CertificatesICertificates2**) |
| [**Retirar**](certificates-remove.md) | Quita un objeto de [**certificado**](certificate.md) único de la colección.<br/> (Se hereda de **CertificatesICertificates2**)                            |
| [**Guardar**](certificates-save.md)     | Guarda los certificados en un archivo especificado.<br/> (Se hereda de **CertificatesICertificates2**)                                                                |
| [**Seleccionar**](certificates-select.md) | Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de los certificados seleccionados.<br/> (Se hereda de **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Propiedades

El objeto de **certificados** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](certificates-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos de [**certificado**](certificate.md) de la colección.<br/>                                                                                                                                |
| [**Elemento**](certificates-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto de [**certificado**](certificate.md) que representa el certificado indizado de la colección. Esta es la propiedad predeterminada.<br/> (Se hereda de **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto de **certificados** y es seguro para el scripting. El ProgID del objeto de **certificados** es "CAPICOM. Certificates. 2 ".

**CAPICOM 1. *x*:** el identificador de programa (ProgID) del objeto de **certificados** es "CAPICOM. Certificates. 1 ".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 

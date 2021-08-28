---
description: 'Objeto Certificates: representa una colección de objetos Certificate.'
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
ms.openlocfilehash: 4ccd66085f96ac7f3567ca3bf993d7d31c9bc70437199701fe88165adf52d03e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126725"
---
# <a name="certificates-object"></a>Objeto Certificates

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto Certificates** representa una colección de [**objetos Certificate.**](certificate.md) Cada [**objeto Certificate**](certificate.md) representa un único certificado [*digital.*](../secgloss/d-gly.md)

El **objeto Certificates** expone las interfaces siguientes:

-   **ICertificates2:** se introdujo en CAPICOM 2.0.
-   **ICertificates:** se introdujo en CAPICOM 1.0.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Certificates** se usa para realizar las siguientes tareas:

-   Agregue o quite un [**objeto Certificate**](certificate.md) a o de la colección.
-   Genere un subconjunto de la colección buscando un conjunto de certificados o mostrando un cuadro de diálogo para seleccionar los certificados.
-   Borre todos los [**objetos Certificate**](certificate.md) de la colección.
-   Recupere el número de certificados de la colección.
-   Recupera un objeto [**Certificate**](certificate.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto Certificates** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Certificates** tiene estos métodos.



| Método                                | Descripción                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Añadir**](certificates-add.md)       | Agrega un [**objeto Certificate**](certificate.md) a la colección.<br/> (Se hereda de **CertificatesICertificates2**)                                        |
| [**Borrar**](certificates-clear.md)   | Quita todos los [**objetos Certificate**](certificate.md) de la colección.<br/> (Se hereda de **CertificatesICertificates2**)                                |
| [**Buscar**](certificates-find.md)     | Devuelve un **objeto Certificates** que contiene todos los certificados que coinciden con los criterios de búsqueda especificados.<br/> (Se hereda de **CertificatesICertificates2**) |
| [**Quitar**](certificates-remove.md) | Quita un único [**objeto Certificate**](certificate.md) de la colección.<br/> (Se hereda de **CertificatesICertificates2**)                            |
| [**Guardar**](certificates-save.md)     | Guarda los certificados en un archivo especificado.<br/> (Se hereda de **CertificatesICertificates2**)                                                                |
| [**Seleccionar**](certificates-select.md) | Muestra un cuadro de diálogo para seleccionar certificados y devuelve una colección de esos certificados seleccionados.<br/> (Se hereda de **CertificatesICertificates2**)  |



 

### <a name="properties"></a>Propiedades

El **objeto Certificates** tiene estas propiedades.



| Propiedad                                             | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Count**](certificates-count.md)<br/>       | Solo lectura<br/> | Recupera el número de [**objetos Certificate**](certificate.md) de la colección.<br/>                                                                                                                                |
| [**Elemento**](certificates-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**Certificate**](certificate.md) que representa el certificado indexado de la colección. Esta es la propiedad predeterminada.<br/> (Se hereda de **CertificatesICertificates2ICertificates**)          |



 

## <a name="remarks"></a>Comentarios

Se puede crear el objeto **Certificates** y es seguro para el scripting. El ProgID del **objeto Certificates** es "CAPICOM. Certificates.2".

**CAPICOM 1. *x:*** el ProgID del **objeto Certificates** es "CAPICOM. Certificates.1".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 

---
description: Representa la plantilla de extensión de certificado del certificado.
ms.assetid: 1ae9220a-f6b3-47c5-bd08-a36ffd84e1f9
title: Objeto de plantilla
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 53c7b06fa4194d0adb4124f3978787f5d1fce0ba88e78ef99dcd6ac162eca2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897326"
---
# <a name="template-object"></a>Objeto de plantilla

\[El **objeto Template** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para plantilla de certificado para recuperar la plantilla de extensión de certificado.\]

El **objeto Template** representa la plantilla de extensión de certificado del certificado.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Template** se usa para realizar las siguientes tareas:

-   Determine si la plantilla está marcada como crítica o presente.
-   Recupere el [*identificador de objeto*](../secgloss/o-gly.md) (OID) o el nombre de la plantilla.
-   Recupere la versión secundaria o principal de la plantilla.

## <a name="members"></a>Miembros

El **objeto Template** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Template** tiene estas propiedades.



| Propiedad                                                 | Tipo de acceso          | Descripción                                                                                            |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------|
| [**IsCritical**](template-iscritical.md)<br/>     | Solo lectura<br/> | Recupera un valor booleano que indica si la extensión de plantilla está marcada como crítica.<br/> |
| [**IsPresent**](template-ispresent.md)<br/>       | Solo lectura<br/> | Recupera un valor booleano que indica si la extensión de plantilla está presente.<br/>         |
| [**MajorVersion**](template-majorversion.md)<br/> | Solo lectura<br/> | Recupera el número de versión principal de la plantilla.<br/>                                         |
| [**MinorVersion**](template-minorversion.md)<br/> | Solo lectura<br/> | Recupera el número de versión secundaria de la plantilla.<br/>                                         |
| [**Nombre**](template-name.md)<br/>                 | Solo lectura<br/> | Recupera una cadena que contiene el nombre de la plantilla.<br/>                                  |
| [**Oid**](template-oid.md)<br/>                   | Solo lectura<br/> | Recupera un objeto [**OID**](oid.md) que identifica el **objeto Template.**<br/>             |



 

## <a name="remarks"></a>Comentarios

No **se puede** crear el objeto Template.

El **método** [**Certificate.Template**](certificate-template.md) devuelve un objeto Template.

CAPICOM usa dos versiones diferentes de plantillas de certificado. En la tabla siguiente se muestra el nombre y el OID de cada versión de plantilla de certificado.



| Versión | Nombre                               | OID                    |
|---------|------------------------------------|------------------------|
| V1      | szOID \_ ENROLL \_ CERTTYPE \_ EXTENSION | "1.3.6.1.4.1.311.20.2" |
| V2      | szOID \_ CERTIFICATE \_ TEMPLATE       | "1.3.6.1.4.1.311.21.7" |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

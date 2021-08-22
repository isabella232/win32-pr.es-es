---
description: Representa una colección de objetos Extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Objeto Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e484de5b4266c5a2458d15365d44a3461a7d1d0589e22391b1afd66e437e02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006843"
---
# <a name="extensions-object"></a>Objeto Extensions

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto Extensions** representa una colección de [**objetos Extension.**](extension.md) Cada [**objeto Extension**](extension.md) representa una única extensión de certificado.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Extensions** se usa para realizar las siguientes tareas:

-   Recupere el número de extensiones de certificado de la colección.
-   Recuperar un objeto [**Extension**](extension.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto Extensions** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Extensions** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](extensions-count.md)<br/>       | Solo lectura<br/> | Recupera el número de [**objetos Extension**](extension.md) de la colección.<br/>                                                                                                                                    |
| [**Elemento**](extensions-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto [**Extension**](extension.md) que representa la extensión de certificado indizada de la colección. Esta es la propiedad predeterminada.<br/>                                                               |



 

## <a name="remarks"></a>Comentarios

El **método Certificate.Extensions** devuelve el [**objeto Extensions.**](certificate-extensions.md)

No **se puede crear** el objeto Extensions.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

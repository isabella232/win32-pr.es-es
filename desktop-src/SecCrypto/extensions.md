---
description: Representa una colección de objetos de extensión.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Extensions (objeto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671021"
---
# <a name="extensions-object"></a>Extensions (objeto)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto **extensions** representa una colección de objetos de [**extensión**](extension.md) . Cada objeto de [**extensión**](extension.md) representa una única extensión de certificado.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **extensiones** se usa para realizar las siguientes tareas:

-   Recupere el número de extensiones de certificado de la colección.
-   Recupera un objeto de [**extensión**](extension.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **extensions** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **extensions** tiene estas propiedades.



| Propiedad                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extensions-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](extensions-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos de [**extensión**](extension.md) de la colección.<br/>                                                                                                                                    |
| [**Elemento**](extensions-item.md)<br/>         | Solo lectura<br/> | Recupera el objeto de [**extensión**](extension.md) que representa la extensión de certificado indizada de la colección. Esta es la propiedad predeterminada.<br/>                                                               |



 

## <a name="remarks"></a>Observaciones

El método [**Certificate. Extensions**](certificate-extensions.md) devuelve el objeto **extensions** .

No se puede crear el objeto **extensions** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

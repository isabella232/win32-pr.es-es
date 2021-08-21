---
description: Representa una extensión de certificado única.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objeto de extensión (Mmcobj.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e311c6dc69f40d32163c70cabf6a38780a989764bd77f4023c61ede5c1ba713c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006963"
---
# <a name="extension-object"></a>Objeto de extensión

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto Extension** representa una única extensión de certificado.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto** Extension se usa para realizar las siguientes tareas:

-   Recupere el OID de la extensión de certificado.
-   Recupere los datos de extensión de certificado representados [**por un objeto EncodedData.**](encodeddata.md)
-   Determine si la extensión de certificado está marcada como crítica.

## <a name="members"></a>Miembros

El **objeto** Extension tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Extension** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso          | Descripción                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | Solo lectura<br/> | Recupera los datos codificados para la extensión.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Solo lectura<br/> | Recupera un valor booleano que indica si la extensión está marcada como crítica.<br/> |
| [**Oid**](extension-oid.md)<br/>                 | Solo lectura<br/> | Recupera el identificador de objeto de la extensión. Esta es la propiedad predeterminada.<br/>   |



 

## <a name="remarks"></a>Comentarios

No **se puede** crear el objeto Extension.

El **objeto de** colección Extensions usa el objeto [**Extensions.**](extensions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>Mmcobj.h</dt> </dl>    |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

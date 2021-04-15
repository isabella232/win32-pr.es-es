---
description: Representa una única extensión de certificado.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objeto de extensión (Mmcobj. h)
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
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690212"
---
# <a name="extension-object"></a>Objeto de extensión

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto de **extensión** representa una única extensión de certificado.

## <a name="when-to-use"></a>Cuándo se usa

El objeto de **extensión** se usa para realizar las siguientes tareas:

-   Recupere el OID de la extensión de certificado.
-   Recupera los datos de la extensión de certificado representados por un objeto [**EncodedData**](encodeddata.md) .
-   Determine si la extensión de certificado está marcada como crítica.

## <a name="members"></a>Miembros

El objeto de **extensión** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto de **extensión** tiene estas propiedades.



| Propiedad                                                | Tipo de acceso          | Descripción                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | Solo lectura<br/> | Recupera los datos codificados para la extensión.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Solo lectura<br/> | Recupera un valor booleano que indica si la extensión está marcada como crítica.<br/> |
| [**OID**](extension-oid.md)<br/>                 | Solo lectura<br/> | Recupera el identificador de objeto de la extensión. Esta es la propiedad predeterminada.<br/>   |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto de **extensión** .

El objeto de la colección de [**extensiones**](extensions.md) utiliza el objeto de **extensión** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Encabezado<br/>                | <dl> <dt>Mmcobj. h</dt> </dl>    |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

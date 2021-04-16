---
description: Representa un puntero de informe de prácticas de certificación (CPS) o el calificador de aviso de usuario.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Objeto de calificador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649861"
---
# <a name="qualifier-object"></a>Objeto de calificador

\[El objeto de **calificador** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]

El objeto **calificador** representa un puntero de declaración de prácticas de certificación (CPS) o un calificador de aviso de usuario.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **calificador** se usa para realizar las siguientes tareas:

-   Recupere el identificador de objeto del calificador.
-   Recupere el identificador uniforme de recursos (URI) que señala a una CPS publicada por la [*entidad de certificación*](../secgloss/c-gly.md) (CA).
-   Recupere el nombre de la organización asociada con el calificador.
-   Recupere el nombre y el contenido de un aviso de usuario.

## <a name="members"></a>Miembros

El objeto **calificador** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **calificador** tiene estas propiedades.



| Propiedad                                                          | Tipo de acceso          | Descripción                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | Solo lectura<br/> | Recupera una cadena que contiene el URI que apunta a una CPS publicada por la CA.<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | Solo lectura<br/> | Recupera una cadena que incluye el contenido del aviso de usuario. Esta propiedad puede estar vacía.<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | Solo lectura<br/> | Recupera un objeto **NoticeNumbers** que contiene la colección de números de aviso de usuario. Esta propiedad puede estar vacía.<br/>    |
| [**OID**](qualifier-oid.md)<br/>                           | Solo lectura<br/> | Recupera un objeto [**OID**](oid.md) que identifica el calificador. Esta es la propiedad predeterminada.<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | Solo lectura<br/> | Recupera una cadena que contiene el nombre de la organización asociada al calificador. Esta propiedad puede estar vacía.<br/> |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto de **calificador** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 

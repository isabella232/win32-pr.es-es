---
description: Codificación y codificación de un contexto de certificado mediante CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codificación y codificación de un contexto de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f640e12034ebf4ec84e0e71013197f043453b62e1102018dcfe9ea887d6ada
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874898"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codificación y codificación de un contexto de certificado

[*CryptoAPI*](../secgloss/c-gly.md) admite la codificación y la codificación de [*certificados*](../secgloss/c-gly.md). CryptoAPI incluye un sistema amplio y flexible de funciones y estructuras de C que permiten codificar y codificar de varias maneras. CryptoAPI admite la estructura de [*certificados X.509*](../secgloss/x-gly.md) estándar y la codificación Standard [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) para proporcionar interoperabilidad con otros sistemas.

Para obtener información general sobre los datos codificados, vea Datos codificados [y descodificados.](encoded-and-decoded-data.md)

## <a name="certificate-contexts"></a>Contextos de certificado

Un contexto [*de*](../secgloss/c-gly.md)certificado , [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context), es una estructura de C que contiene un miembro codificado, un identificador para un almacén de certificados [*,*](../secgloss/c-gly.md)un puntero al [*blob*](../secgloss/c-gly.md)de certificado codificado original y un puntero a una estructura [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) C.

La [**estructura \_ CERT INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) es el núcleo del certificado. Contiene, en forma directa y en formato codificado, toda la información básica del certificado. En la ilustración siguiente se muestra **la estructura CERT \_ INFO** con todos sus miembros codificados como sombreados.

![cert \- info structure](images/certinf2.png)

Los **miembros IssuerUniqueID** y **SubjectUniqueID** forman parte de la implementación del certificado [*X.509*](../secgloss/x-gly.md) versión 2, pero rara vez se usan. Las extensiones de certificado de la versión 3 reemplazan la funcionalidad de estos miembros.

Si se necesita la información contenida en los miembros codificados (sombreados) **Issuer** y **Subject,** esos miembros deben descodificarse. Use [**CryptDecodeObject para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) descodificar estos miembros. En la ilustración siguiente se muestra el proceso de decodificación de uno de estos miembros.

![descodificación con cryptdecodeobject](images/infoflow.png)

En el caso ilustrado, la función [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) crea una estructura [**CERT NAME \_ \_ INFO,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) una matriz de estructuras [**DE CERT \_ RDN,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) una matriz correspondiente de estructuras [**CERT \_ RDN \_ ATTR**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) y una cadena que contiene el nombre. Los miembros de **la estructura CERT \_ RDN \_ ATTR** determinan el contenido de la cadena. Por ejemplo, si el **miembro pszObjId** es 2.5.4.3, la cadena contiene un nombre común. Si es 2.5.4.10, la cadena contendrá un nombre de organización. Para obtener una lista de [*estos identificadores de objeto*](../secgloss/o-gly.md) (OVD), vea CERT **\_ RDN \_ ATTR**.

El **miembro dwValueType** contiene información sobre el tipo de cadena. Si es CERT RDN PRINTABLE STRING, el miembro de valor contiene una cadena de caracteres terminada en cero y de ancho \_ \_ de \_ bytes. Si es CERT \_ RDN UNICODE STRING, la cadena es una cadena de caracteres de doble ancho (tamaño de \_ \_ palabra).

Para obtener un proceso detallado de codificación y codificación de certificados, vea Codificar una estructura [DE \_ INFORMACIÓN](encoding-a-cert-info-structure.md) DE CERT y [Decoding a CERT \_ INFO Structure](decoding-a-cert-info-structure.md).

 

 

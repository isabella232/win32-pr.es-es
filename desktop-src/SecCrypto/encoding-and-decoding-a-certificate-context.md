---
description: Codificar y descodificar un contexto de certificado mediante CryptoAPI.
ms.assetid: 149d1097-5f50-40ba-84f1-b815f54ba33d
title: Codificar y descodificar un contexto de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4168d15ad8db5d4711a18f2042106e7d6d46010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275752"
---
# <a name="encoding-and-decoding-a-certificate-context"></a>Codificar y descodificar un contexto de certificado

[*CryptoAPI*](../secgloss/c-gly.md) admite la codificación y la descodificación de [*certificados*](../secgloss/c-gly.md). CryptoAPI incluye un sistema amplio y flexible de funciones y estructuras de C que permiten codificar y descodificar de varias maneras. CryptoAPI admite la estructura de certificados [*X. 509*](../secgloss/x-gly.md) estándar y la codificación de [*notación de sintaxis abstracta*](../secgloss/a-gly.md) estándar (ASN. 1) para proporcionar interoperabilidad con otros sistemas.

Para obtener información general sobre los datos codificados, vea [datos codificados y descodificados](encoded-and-decoded-data.md).

## <a name="certificate-contexts"></a>Contextos de certificado

Un [*contexto*](../secgloss/c-gly.md)de certificado [**, \_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)de certificado, es una estructura de C que contiene un miembro codificado, un identificador de un [*almacén de certificados*](../secgloss/c-gly.md), un puntero al BLOB de [*certificado*](../secgloss/c-gly.md)codificado original y un puntero a una estructura de [**\_ información**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) de certificado C.

La estructura de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) es el corazón del certificado. Contiene, en forma directa y codificada, toda la información básica del certificado. En la ilustración siguiente se muestra la estructura de **\_ información de certificado** con todos sus miembros codificados mostrados como sombreados.

![estructura de información de certificado \-](images/certinf2.png)

Los miembros **IssuerUniqueID** y **SubjectUniqueID** forman parte de la implementación del certificado [*X. 509*](../secgloss/x-gly.md) versión 2, pero rara vez se usan. Las extensiones de certificado de la versión 3 reemplazan la funcionalidad de estos miembros.

Si la información contenida en los miembros codificados (sombreados) y el **emisor** son necesarios, esos **miembros se deben** descodificar. Use [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) para descodificar estos miembros. En la ilustración siguiente se muestra el proceso de descodificación de uno de estos miembros.

![descodificación con cryptdecodeobject](images/infoflow.png)

En el caso de la ilustración, la función [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) crea una estructura de [**información de \_ nombre \_ de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_name_info) , una matriz de estructuras [**\_ RDN de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn) , una matriz correspondiente de estructuras de [**\_ \_ atributo RDN de CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn_attr) y una cadena que contiene el nombre. Los miembros de la estructura **CERT \_ RDN \_ ATTR** determinan el contenido de la cadena. Por ejemplo, si el miembro **pszObjId** es 2.5.4.3, la cadena contiene un nombre común. Si es 2.5.4.10, la cadena contendría un nombre de la organización. Para obtener una lista de estos [*identificadores de objeto*](../secgloss/o-gly.md) (OID), consulte **CERT \_ RDN \_ ATTR**.

El miembro **dwValueType** contiene información sobre el tipo de cadena. Si se trata de \_ \_ una cadena imprimible de RDN de CERT \_ , el miembro de valor contiene una cadena de caracteres de ancho byte y terminada en cero. Si se trata de \_ \_ una cadena Unicode RDN CERT \_ , la cadena es una cadena de caracteres de doble ancho (de tamaño de palabra).

Para obtener un proceso detallado de codificación y descodificación de certificados, consulte [codificación de una \_ estructura de información de certificado](encoding-a-cert-info-structure.md) y [descodificación de una estructura de \_ información de certificado](decoding-a-cert-info-structure.md).

 

 

---
description: Dado un certificado, el primer paso para descodificar el BLOB de certificado es llamar a CertCreateCertificateContext, pasándole un puntero al certificado codificado (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Descodificar una estructura de CERT_INFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7178c9a5bcfc95a8e2945a6e381f0c2c29cf3b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557255"
---
# <a name="decoding-a-cert_info-structure"></a>Descodificar una \_ estructura de información de certificado

Dado un certificado, el primer paso para descodificar el [*BLOB*](../secgloss/b-gly.md) de certificado es llamar a [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext), pasándole un puntero al certificado codificado (*BLOB*). Cuando se llama a esta función, se crea un duplicado del certificado codificado, se crea una estructura de tipo de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)y se crea una estructura de tipo de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Como se muestra en la siguiente ilustración, un [*contexto de certificado*](../secgloss/c-gly.md) incluye el *BLOB* de certificado original, una estructura de c de tipo de **\_ contexto** de certificado y una estructura de c de tipo **\_ información de certificado**. Uno de los miembros de la estructura de **\_ contexto CERT** apunta a la estructura de **\_ información de certificado** y a otra al BLOB de certificado codificado.

![contexto de certificado](images/certcntx.png)

El objeto codificado (miembro de datos) siempre se proporciona como entrada a la función [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) y el resultado es una estructura de C que puede tener o no miembros codificados, en función de la distancia del proceso en el que se encuentre.

Hay otro miembro que requiere cierta descodificación y que es el miembro de la **extensión** . Aunque no está codificado en el nivel de [**\_ información del certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , contiene información codificada. Para descodificar esta información, continúe como se muestra en la siguiente ilustración.

![descodificar información](images/xtension.png)

En la estructura de [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) , el miembro **rgExtension** es un puntero a una matriz de estructuras de [**\_ extensión de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) . Cada estructura de **\_ extensión de certificado** tiene un miembro de **valor** que está codificado y debe descodificarse. El miembro de **valor** se pasa a la función [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) y, a continuación, la salida de la función depende del valor del miembro **pszObjId** . Observe que, en la ilustración, se generan dos estructuras diferentes, una de [**tipo \_ \_ \_ información de restricciones básicas de CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) y otra de [**tipo \_ \_ información de \_ identificador \_ de clave de entidad emisora**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), según el valor de **pszObjId**.

 

 

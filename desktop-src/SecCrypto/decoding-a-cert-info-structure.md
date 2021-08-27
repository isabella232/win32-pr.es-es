---
description: Dado un certificado, el primer paso para descodificar el blob de certificado es llamar a CertCreateCertificateContext y pasarle un puntero al certificado codificado (BLOB).
ms.assetid: b50530e2-15a0-4215-bf18-300cf67d1611
title: Decoding a CERT_INFO Structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8eab5a75c2a5906ac875f925845f83f3c411c12a31aeea4825efd795b78eaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100895"
---
# <a name="decoding-a-cert_info-structure"></a>Decoding a CERT \_ INFO Structure

Dado un certificado, el primer paso para descodificar el [*blob*](../secgloss/b-gly.md) de certificado es llamar a [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)y pasarle un puntero al certificado codificado *(BLOB).* Cuando se llama a esta función, crea un duplicado del certificado codificado, crea una estructura de tipo [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)y crea una estructura de tipo [**CERT \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info). Como se muestra en [](../secgloss/c-gly.md) la ilustración siguiente, un contexto de certificado incluye el *blob* de certificado original, una estructura C de tipo **CERT \_ CONTEXT** y una estructura C de tipo **CERT \_ INFO**. Uno de los miembros de la estructura **CERT \_ CONTEXT** apunta a la estructura **CERT \_ INFO** y otro al blob de certificado codificado.

![contexto de certificado](images/certcntx.png)

El objeto codificado (miembro de datos) siempre se proporciona como entrada para la función [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) y la salida es una estructura de C que puede o no tener miembros codificados, dependiendo de la distancia en el proceso que se esté.

Hay otro miembro que requiere alguna decodación y que es el miembro **Extension.** Aunque no está codificada en el nivel [**CERT \_ INFO,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) contiene información codificada. Para descodificar esta información, continúe como se muestra en la ilustración siguiente.

![decoding information](images/xtension.png)

En la [**estructura CERT \_ INFO,**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) el **miembro rgExtension** es un puntero a una matriz de estructuras [**DE EXTENSIÓN \_ CERT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) Cada **estructura DE EXTENSIÓN \_ CERT** tiene un **miembro Value** que está codificado y debe descodificarse. El **miembro Value** se pasa a la función [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) y, a continuación, la salida de la función depende del valor del miembro **pszObjId.** Observe que, en la ilustración, se generan dos estructuras diferentes, una de tipo [**CERT \_ BASIC \_ CONSTRAINTS \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_basic_constraints_info) y una de tipo [**CERT AUTHORITY KEY ID \_ \_ \_ \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info), en función del valor **de pszObjId**.

 

 

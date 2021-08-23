---
description: A partir del formato de certificado X.509 versión 3, un certificado puede contener extensiones de certificado.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Controladores de extensiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba61c5896887471038325eba0dbed75f43061cff81452727933a3013c37f8aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006933"
---
# <a name="extension-handlers"></a>Controladores de extensiones

A partir [*del formato de certificado X.509*](../secgloss/x-gly.md) versión 3, un certificado puede contener extensiones de certificado. (Para obtener el contenido de un certificado X.509, vea [Propiedades del certificado).](certificate-properties.md) Estas extensiones indican información adicional. Por ejemplo, una extensión puede indicar información adicional de identificación del sujeto o puede indicar información de uso de clave, que especifica las tareas (como firma o cifrado) para las que se puede usar una clave. Se define un conjunto de extensiones estándar para el uso de la aplicación, y las extensiones también se pueden personalizar.

Cada extensión tiene una cadena de identificador de objeto asociada que identifica el tipo de información adicional y una estructura de datos que contiene esta información. Por ejemplo, el identificador de objeto de uso de clave es "2.5.29.15", que indica la información de uso de claves. Su estructura de datos asociada es [**un CRYPT \_ BIT \_ BLOB**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (campo de bits) que especifica cómo se puede usar la clave.

Se puede agregar una extensión a un certificado antes de que se emita. Cuando se emite el certificado, las extensiones habilitadas forman parte del certificado. Si una extensión está marcada como crítica, la aplicación debe conocer su uso y la aplicación debe cumplir la intención o el valor de la extensión. Servicios de certificados permite establecer extensiones en un certificado no emitido a través de los métodos proporcionados por [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) [**e ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy). Para más información sobre las extensiones de certificado, consulte [**EXTENSIÓN \_ CERT en**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) la documentación de CryptoAPI. Para obtener información sobre las estructuras de datos de extensión de certificado comunes, vea Estructuras de extensión de [certificado X.509](cryptography-structures.md).

El controlador de extensiones es un objeto COM que proporciona rutinas para codificar las extensiones y los tipos de datos más complejos, pero usados con frecuencia, como IA5String o PrintableString.

Las extensiones que tienen los tipos de datos **DATE,** **LONG** y **BSTR** no requieren un controlador de extensión. El módulo de directivas simplemente llama a [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) con el parámetro *Type* establecido en un valor que representa el tipo de datos de extensión: PROPTYPE \_ DATE, PROPTYPE LONG o \_ PROPTYPE \_ STRING. A continuación, pasa la extensión al motor del servidor. El motor de servidor, a su vez, realiza la codificación [*abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) antes de almacenar la extensión en el certificado.

Sin embargo, las extensiones que tienen tipos de datos distintos de estos tipos predeterminados deben estar codificadas por ASN.1 por un controlador de extensiones antes de que el módulo de directivas los pase al motor del servidor. Cuando el módulo de directiva llama a [**ICertServerPolicy::SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) para pasar una extensión codificada con ASN.1 al motor de servidor, debe establecer el parámetro *Type* en PROPTYPE \_ BINARY. A continuación, el motor del servidor simplemente almacena esta extensión codificada en el certificado.

El controlador de extensión predeterminado, Certenc.dll, exporta una serie de interfaces **ICertEncodeXXX** y el módulo de directivas puede llamarlo. La información de tipo necesaria también se incluye en Certencl.dll que se proporciona en el Kit de desarrollo de software de plataforma (SDK). Cada interfaz proporciona un **método Encode** que devuelve una extensión de certificado codificada con ASN.1 al módulo de directivas en formato binario. A continuación, el módulo de directivas puede establecer la extensión en un certificado llamando al [**método ICertServerPolicy::SetCertificateExtension.**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension)

Para obtener más información, vea [Escribir controladores de extensión personalizados.](writing-custom-extension-handlers.md)

 

 

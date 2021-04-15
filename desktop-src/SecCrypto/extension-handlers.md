---
description: A partir de la versión 3 del formato de certificado X. 509, un certificado puede contener extensiones de certificado.
ms.assetid: fb106cab-8a61-4a83-8fb4-7c045d905575
title: Controladores de extensión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfcf1b47fcc97b87f5956f4584aee07acce04222
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688538"
---
# <a name="extension-handlers"></a>Controladores de extensión

A partir de la versión 3 del formato de certificado [*X. 509*](../secgloss/x-gly.md) , un certificado puede contener extensiones de certificado. (Para obtener el contenido de un certificado X. 509, consulte [propiedades de certificado](certificate-properties.md)). Estas extensiones indican información adicional. Por ejemplo, una extensión puede indicar información de identificación de asunto adicional o puede indicar información de uso de claves, que especifica las tareas (como la firma o el cifrado) para las que se puede usar una clave. Se define un conjunto de extensiones estándar para el uso de la aplicación, y las extensiones también se pueden personalizar.

Cada extensión tiene una cadena de identificador de objeto asociada que identifica el tipo de información adicional y una estructura de datos que contiene esta información. Por ejemplo, el identificador de objeto de uso de clave es "2.5.29.15", que indica la información de uso de claves. La estructura de datos asociada es [**un \_ \_ BLOB de bit cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_bit_blob) (campo de bits) que especifica cómo se puede usar la clave.

Una extensión se puede Agregar a un certificado antes de que se emita. Cuando se emite el certificado, las extensiones habilitadas forman parte del certificado. Si una extensión se marca como crítica, su uso debe ser conocido por la aplicación que usa y la aplicación debe adherirse a la intención o el valor de la extensión. Los servicios de Certificate Server permiten que las extensiones se establezcan en un certificado no emitido a través de los métodos proporcionados por [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) y [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy). Para obtener más información acerca de las extensiones de certificado, consulte [**\_ extensión**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_extension) de certificado en la documentación de CryptoAPI. Para obtener información sobre las estructuras de datos de extensión de certificado comunes, vea [estructuras de extensión de certificados X. 509](cryptography-structures.md).

El controlador de extensión es un objeto COM que proporciona rutinas para codificar las extensiones y los tipos de datos más complejos, pero usados comúnmente, como IA5String o PrintableString.

Las extensiones que tienen los tipos de datos **Date**, **Long** y **BSTR** no requieren un controlador de extensión. El módulo de directivas simplemente llama a [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) con el parámetro de *tipo* establecido en un valor que representa el tipo de datos de la extensión: PROPTYPE \_ Date, PROPTYPE \_ Long o PROPTYPE \_ String. A continuación, pasa la extensión al motor del servidor. A su vez, el motor de servidor realiza la codificación de la [*notación de sintaxis abstracta uno*](../secgloss/a-gly.md) (ASN. 1) antes de almacenar la extensión en el certificado.

Sin embargo, las extensiones que tienen tipos de datos distintos de estos tipos predeterminados deben ser ASN. 1 codificado por un controlador de extensión antes de que el módulo de directivas las pase al motor de servidor. Cuando el módulo de directivas llama a [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) para pasar una extensión con codificación ASN. 1 al motor del servidor, debe establecer el parámetro de *tipo* en PROPTYPE \_ Binary. A continuación, el motor de servidor simplemente almacena esta extensión codificada en el certificado.

El controlador de extensión predeterminado, Certenc.dll, exporta varias interfaces **ICertEncodeXXX** y el módulo de directivas puede llamarlas. La información de tipo necesaria también se incluye en Certencl.dll que se proporciona en el kit de desarrollo de software (SDK) de la plataforma. Cada interfaz proporciona un método de **codificación** que devuelve una extensión de certificado con codificación ASN. 1 al módulo de directivas en formato binario. Después, el módulo de directivas puede establecer la extensión en un certificado llamando al método [**ICertServerPolicy:: SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) .

Para obtener más información, vea [Escribir controladores de extensión personalizados](writing-custom-extension-handlers.md).

 

 

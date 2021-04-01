---
description: En este tema se enumeran las consideraciones para usar la API de firma digital XPS para agregar firmas digitales a un documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso de la API de firma digital XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9037a1442a44b082caec21309c94390b3f783e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909573"
---
# <a name="using-xps-digital-signature-api"></a>Uso de la API de firma digital XPS

En este tema se enumeran las consideraciones para usar la API de firma digital XPS para agregar firmas digitales a un documento XPS.

La API de firma digital XPS permite a las aplicaciones solicitar a los usuarios que firmen documentos XPS y comprobar las firmas que se encuentran en los documentos XPS. La API de firma digital XPS se puede aplicar a un documento XPS sin cargarlo en un OM XPS y se puede usar en flujos de documento XPS que se serializan desde un OM XPS.

La sección tareas de programación de la [API de firma digital XPS](#xps-digital-signature-api-programming-tasks) contiene temas que describen cómo programar con la API de firma digital XPS. En este tema se enumeran las siguientes consideraciones sobre el uso de la API de firma digital XPS al agregar compatibilidad con firmas digitales a una aplicación.

-   [Tareas de programación de la API de firma digital XPS](#xps-digital-signature-api-programming-tasks)
-   [Notas especiales sobre la programación de la API de firma digital XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Comprobar las firmas digitales en un documento XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Directiva de firma de firma digital](#digital-signature-signing-policy)
    -   [Incrustar una cadena de certificados](#embedding-a-certificate-chain)
    -   [Usar la \_ estructura de contexto CERT](#using-the-cert\_context-structure)
-   [Temas relacionados](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Tareas de programación de la API de firma digital XPS

Esta sección contiene temas que describen cómo realizar tareas de programación con la API de firma digital XPS.

-   [Tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md)<dl>

[Inicializar el administrador de firmas](initialize-the-signature-manager.md)  
    [Firmar un documento](sign-a-document.md)  
    [Agregar una solicitud de firma a un documento XPS](add-a-signature-request-to-a-document.md)  
    [Comprobar las firmas del documento](verify-document-signatures.md)  
    </dl>
-   [Tareas adicionales de programación de firmas digitales](advanced-digital-signature-programming-tasks.md)<dl>

[Cargar un certificado desde un archivo](load-a-certificate-from-a-file.md)  
    [Comprobar que un certificado admite un método de firma](verify-a-certificate-supports-a-signature-method.md)  
    [Comprobar que el sistema admite un método de síntesis](verify-a-certificate-supports-a-digest-method.md)  
    [Insertar cadenas de certificado en un documento](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Notas especiales sobre la programación de la API de firma digital XPS

Los temas siguientes requieren una consideración especial al usar la API de firma digital XPS.

-   [Comprobar las firmas digitales en un documento XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Directiva de firma de firma digital](#digital-signature-signing-policy)
-   [Incrustar una cadena de certificados](#embedding-a-certificate-chain)
-   [Usar la \_ estructura de contexto CERT](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Comprobar las firmas digitales en un documento XPS

[**IXpsSignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) comprueba solo el contenido firmado para determinar que no ha cambiado desde que se firmó. **IXpsSignature:: Verify** no comprueba ninguno de los certificados que se usaron para firmar el contenido del documento.

Para obtener más información acerca de los certificados y la criptografía, consulte [acerca de la criptografía](/windows/desktop/SecCrypto/about-cryptography).

Para ver un ejemplo de cómo comprobar las firmas de documento en un programa, consulte [comprobación de firmas y certificados de documento](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Directiva de firma de firma digital

La Directiva de firma de firmas digitales determina qué partes de un documento XPS están firmadas. Una opción de directiva de firma es firmar las relaciones de firma que se inician desde la parte del origen de la firma. Dado que las relaciones de firma cambian con cada firma que se agrega, las firmas que se realicen en esta Directiva se interrumpirán cuando se agreguen nuevas firmas. Asegúrese de que comprende claramente las implicaciones y los efectos de la configuración de esta Directiva; de lo contrario, podría producirse un comportamiento inesperado o no deseado.

Para obtener más información acerca de las directivas de firma, consulte [**\_ \_ Directiva**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)de firma de XPS.

### <a name="embedding-a-certificate-chain"></a>Incrustar una cadena de certificados

Los certificados que componen la cadena de confianza de un certificado específico se pueden agregar a un documento XPS. La inserción de estos certificados puede facilitar, en escenarios sin conexión, que una aplicación Compruebe los certificados que usa una firma digital.

Para obtener más información sobre cómo insertar certificados en un documento XPS, consulte [Insertar cadenas de certificados en un documento](embedding-certificate-trust-chains-in-a-document.md).

### <a name="using-the-cert_context-structure"></a>Usar la \_ estructura de contexto CERT

Las estructuras de [**\_ contexto**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) de certificado y de [**\_ información de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) son las estructuras de datos principales que contienen información de certificado. Para obtener más información sobre el uso de estas estructuras, vea [usar una \_ estructura de datos de información de certificado](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**Certificado \_ de**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Las estructuras de contexto devueltas por las funciones de Crypto API deben liberarse cuando ya no se necesiten. Para liberar una estructura de **\_ contexto de certificado** , llame a la función [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Tareas adicionales de programación de firmas digitales](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**contexto de certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**información de certificado \_**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**\_Directiva de firma de XPS \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

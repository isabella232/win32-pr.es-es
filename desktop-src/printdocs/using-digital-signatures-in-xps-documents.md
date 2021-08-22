---
description: En este tema se enumeran las consideraciones para usar XPS Digital Signature API para agregar firmas digitales a un documento XPS.
ms.assetid: 27c28313-d8db-4c40-9972-cb03bdaa125c
title: Uso de la API de firma digital XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ea6e38704efa2a348a90fec247f37b9722857a3838b10233937e63dc37fdbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118469359"
---
# <a name="using-xps-digital-signature-api"></a>Uso de la API de firma digital XPS

En este tema se enumeran las consideraciones para usar XPS Digital Signature API para agregar firmas digitales a un documento XPS.

XPS Digital Signature API permite a las aplicaciones solicitar a los usuarios que firmen documentos XPS y comprueben las firmas que se encuentran en los documentos XPS. La API de firma digital xps se puede aplicar a un documento XPS sin cargarlo en un OM xps y se puede usar en secuencias de documentos XPS que se serializan desde un OM xps.

La [sección XpS Digital Signature API Programming Tasks](#xps-digital-signature-api-programming-tasks) contiene temas que describen cómo programar con XPS Digital Signature API. En este tema se enumeran las consideraciones siguientes para usar la API de firma digital XPS al agregar compatibilidad con firmas digitales a una aplicación.

-   [Tareas de programación de API de firma digital XPS](#xps-digital-signature-api-programming-tasks)
-   [Notas especiales sobre la programación de API de firma digital XPS](#special-notes-about-xps-digital-signature-api-programming)
    -   [Comprobación de firmas digitales en un documento XPS](#verifying-digital-signatures-in-an-xps-document)
    -   [Directiva de firma de firma digital](#digital-signature-signing-policy)
    -   [Inserción de una cadena de certificados](#embedding-a-certificate-chain)
    -   [Usar la estructura CERT \_ CONTEXT](#using-the-cert\_context-structure)
-   [Temas relacionados](#related-topics)

## <a name="xps-digital-signature-api-programming-tasks"></a>Tareas de programación de API de firma digital XPS

Esta sección contiene temas que describen cómo realizar tareas de programación mediante XPS Digital Signature API.

-   [Tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md)<dl>

[Inicializar el Administrador de firmas](initialize-the-signature-manager.md)  
    [Firmar un documento](sign-a-document.md)  
    [Agregar una solicitud de firma a un documento XPS](add-a-signature-request-to-a-document.md)  
    [Comprobar firmas de documento](verify-document-signatures.md)  
    </dl>
-   [Tareas adicionales de programación de firmas digitales](advanced-digital-signature-programming-tasks.md)<dl>

[Cargar un certificado desde un archivo](load-a-certificate-from-a-file.md)  
    [Comprobar que un certificado admite un método signature](verify-a-certificate-supports-a-signature-method.md)  
    [Comprobar que el sistema admite un método de resumen](verify-a-certificate-supports-a-digest-method.md)  
    [Insertar cadenas de certificados en un documento](embedding-certificate-trust-chains-in-a-document.md)  
    </dl>

## <a name="special-notes-about-xps-digital-signature-api-programming"></a>Notas especiales sobre la programación de API de firma digital XPS

Los temas siguientes requieren una consideración especial al usar la API de firma digital XPS.

-   [Comprobación de firmas digitales en un documento XPS](#verifying-digital-signatures-in-an-xps-document)
-   [Directiva de firma de firma digital](#digital-signature-signing-policy)
-   [Inserción de una cadena de certificados](#embedding-a-certificate-chain)
-   [Usar la estructura CERT \_ CONTEXT](#using-the-cert\_context-structure)

### <a name="verifying-digital-signatures-in-an-xps-document"></a>Comprobación de firmas digitales en un documento XPS

[**IXpsSignature::Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) comprueba solo el contenido firmado para determinar que no ha cambiado desde que se firmó. **IXpsSignature::Verify** no comprueba ninguno de los certificados que se usaron para firmar el contenido del documento.

Para obtener más información sobre los certificados y la criptografía, vea [Acerca de la criptografía.](/windows/desktop/SecCrypto/about-cryptography)

Para obtener un ejemplo de cómo comprobar las firmas de documento en un programa, vea [Verify Document Signatures and Certificates](verify-document-signatures.md).

### <a name="digital-signature-signing-policy"></a>Directiva de firma de firma digital

La directiva de firma de firma digital determina qué partes de un documento XPS están firmadas. Una opción de directiva de firma es firmar las relaciones de firma que comienzan desde la parte de origen de la firma. Dado que las relaciones de firma cambian con cada firma que se agrega, las firmas que se realizan en esta directiva se interrumpirán cuando se agregan nuevas firmas. Asegúrese de comprender claramente las implicaciones y efectos de establecer esta directiva. de lo contrario, podría producirse un comportamiento inesperado o no deseado.

Para obtener más información sobre las directivas de firma, vea [**XPS \_ SIGN \_ POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy).

### <a name="embedding-a-certificate-chain"></a>Inserción de una cadena de certificados

Los certificados que son la cadena de confianza de un certificado específico se pueden agregar a un documento XPS. La inserción de estos certificados puede facilitar, en escenarios fuera de línea, que una aplicación compruebe los certificados que usa una firma digital.

Para obtener más información sobre cómo insertar certificados en un documento XPS, vea [Insertar cadenas de certificados en un documento.](embedding-certificate-trust-chains-in-a-document.md)

### <a name="using-the-cert_context-structure"></a>Usar la estructura CERT \_ CONTEXT

Las [**estructuras CERT CONTEXT \_ y**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) [**CERT \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info) son las estructuras de datos principales que contiene información de certificado. Para obtener más información sobre el uso de estas estructuras, vea [Usar una estructura de datos CERT \_ INFO](/windows/desktop/SecCrypto/using-a-cert-info-data-structure).

[**CERT \_ Las**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) estructuras CONTEXT que devuelven las funciones de Crypto API deben liberarse cuando ya no sean necesarias. Para liberar una **estructura CERT \_ CONTEXT,** llame a [**la función CertFreeCertificateContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tareas comunes de programación de firmas digitales](basic-digital-signature-programming-tasks.md)
</dt> <dt>

[Tareas adicionales de programación de firmas digitales](advanced-digital-signature-programming-tasks.md)
</dt> <dt>

[**CONTEXTO \_ DE CERT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**INFORMACIÓN \_ DEL CERTIFICADO**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_info)
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**XPS \_ SIGN \_ POLICY**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 

---
description: 'La comunicación segura a través de redes no seguras suele implicar tres áreas principales de preocupación: privacidad, autenticación e integridad.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Conceptos de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1909cf999bd5eb2f91bd5c7e0243b13969e692792c4ff32804e7c9a7d2940b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876165"
---
# <a name="cryptography-concepts"></a>Conceptos de criptografía

La comunicación segura a través de redes no seguras suele implicar tres áreas principales de [preocupación:](#privacy)privacidad, [autenticación](#authentication)e [integridad.](#integrity) La API de criptografía de Microsoft [*(CryptoAPI)*](../secgloss/c-gly.md)es un conjunto de funciones, interfaces y herramientas que las aplicaciones pueden usar para mejorar la confianza de seguridad en estas áreas.

Además de la funcionalidad de privacidad, autenticación e integridad, [*CryptoAPI*](../secgloss/c-gly.md) también proporciona:

-   Codificación de mensajes en el formulario Abstract [*Syntax Notation One*](../secgloss/a-gly.md) (ASN.1).
-   Decoding ASN.1 messages(Decoding ASN.1 messages).
-   Administrar colecciones de [*certificados en almacenes*](../secgloss/c-gly.md) de [*certificados*](../secgloss/c-gly.md).
-   Trabajar con [*listas de certificados de confianza*](../secgloss/c-gly.md) y cadenas de certificados para comprobar la validez de los certificados.

## <a name="privacy"></a>Privacidad

Para lograr la privacidad, los usuarios deben impedir que cualquier persona, excepto el destinatario previsto, lea un mensaje. La mejora de la probabilidad de privacidad suele implicar el uso de algún tipo [*de criptografía*](../secgloss/c-gly.md). Las técnicas criptográficas se usan para cifrar (codificar) los mensajes antes de almacenar o transmitir los mensajes.

El cifrado de datos transforma [*el texto no cifrado*](../secgloss/p-gly.md) en texto [*cifrado.*](../secgloss/c-gly.md) Los datos que se cifran pueden ser [*texto ASCII,*](../secgloss/a-gly.md) un archivo de base de datos o cualquier otro dato. En esta documentación, el término [*mensaje*](../secgloss/m-gly.md) se usa para hacer referencia a cualquier fragmento  de datos, el texto no cifrado hace referencia a los datos que no se han cifrado y el texto cifrado hace referencia a los datos cifrados. Un buen sistema de cifrado de datos dificulta la transformación de los datos cifrados a texto sin formato sin una clave secreta.

Los datos cifrados se pueden almacenar en medios no seguros o transmitirse a través de una red no segura. Más adelante, los datos se pueden descifrar en su forma original. Este proceso se muestra en la ilustración siguiente.

![ayudar a conservar la privacidad a lo largo del cifrado y descifrado](images/capi01.png)

Cuando se cifran los datos, el mensaje y una [*clave de*](../secgloss/e-gly.md) cifrado se pasan al algoritmo de cifrado. Para descifrar los datos, el texto cifrado y una clave [*de*](../secgloss/d-gly.md) descifrado se pasan al algoritmo de descifrado. El cifrado y descifrado se pueden realizar mediante una sola clave en un proceso denominado cifrado simétrico.

Las claves usadas para descifrar un mensaje deben mantenerse como secretas y seguras lo más posible, y deben transmitirse a otros usuarios mediante técnicas de mejora de la seguridad. Esto se describe más detalladamente en [Cifrado y descifrado de datos.](data-encryption-and-decryption.md) El principal desafío es restringir correctamente el acceso a la clave de descifrado porque cualquier persona que la posea podrá descifrar todos los mensajes cifrados con su clave de cifrado correspondiente.

Para abordar los objetivos de privacidad indicados, los desarrolladores pueden usar [*CryptoAPI*](../secgloss/c-gly.md) para cifrar y firmar digitalmente los datos de forma flexible, al tiempo que ayudan a proporcionar protección para los datos confidenciales de clave privada del usuario.

[*CryptoAPI*](../secgloss/c-gly.md) proporciona las siguientes áreas de funcionalidad para realizar las tareas de cifrado/descifrado, firma de mensajes y almacenamiento de claves:

-   [Funciones de criptografía base](cryptography-functions.md)
-   [Funciones de mensaje simplificadas](cryptography-functions.md)
-   [Funciones de mensaje de bajo nivel](cryptography-functions.md)

## <a name="authentication"></a>Authentication

Las comunicaciones seguras requieren que las personas que se comunican conozcan la identidad de las personas con las que se comunican. La autenticación es el proceso de comprobar la identidad de una persona o entidad.

Por ejemplo, en la vida diaria, la documentación física, a menudo denominada credenciales, se usa para comprobar la identidad de una persona. Cuando se cobra un control, la persona que cobra el control puede pedir que vea una licencia de conducir. La licencia de conductor es un documento físico que aumenta la confianza del comerciante en la identidad de la persona que cobra el control. En este caso, la persona que cobra la comprobación confía en que el estado que emite la licencia ha comprobado correctamente la identidad del titular de la licencia.

Passports proporciona otro ejemplo. Un oficial de la oficina examina un pasaporte y lo acepta como prueba de que una persona es quien dice ser. El oficial confía en que el gobierno hizo un trabajo adecuado para identificar al titular del pasaporte antes de emitir el pasaporte. En ambos ejemplos, existe un nivel de confianza en el emisor del documento físico.

La autenticación también implica asegurarse de que los datos recibidos son los datos enviados. Si la parte A envía un mensaje a la parte B, la parte B debe poder demostrar que el mensaje recibido fue el mensaje que envió la entidad A y no un mensaje que se sustituyó por ese mensaje. Para proporcionar esta forma de autenticación, [*CryptoAPI*](../secgloss/c-gly.md) proporciona funciones para firmar datos y comprobar firmas mediante pares de claves pública y privada.

Dado que las comunicaciones a través de una red de equipo se llevan a cabo sin contacto físico entre los comunicadores, la comprobación de la identidad a menudo depende de una credencial que se puede enviar y recibir a través de una red. Un emisor de credenciales de confianza debe emitir dicha credencial. Los certificados digitales, normalmente conocidos como certificados, son simplemente una credencial de este tipo. Son una manera de comprobar la identidad y lograr la autenticación en una red de equipo.

Un certificado digital es una credencial emitida por una organización o entidad de confianza denominada entidad de certificación (CA). Esta credencial contiene una clave pública (consulte [Pares](public-private-key-pairs.md)de claves públicas y privadas) y datos que identifican el asunto del certificado. Una ca emite un certificado solo después de que la ca haya comprobado la identidad del sujeto del certificado y haya confirmado que la clave pública incluida con el certificado pertenece a ese sujeto.

La comunicación entre una ENTIDAD de certificación y un solicitante de certificados podría realizarla el solicitante que lleva físicamente la información necesaria, quizás almacenada en un disquete, a la CA. Sin embargo, la comunicación normalmente se realiza con un mensaje firmado enviado a través de una red. A menudo, la entidad de certificación usa una aplicación de confianza denominada servidor de certificados para emite certificados.

[*CryptoAPI admite*](../secgloss/c-gly.md) la autenticación mediante el uso de certificados digitales, con funciones de codificación/descodificación de certificados y funciones de [*almacén de*](../secgloss/c-gly.md) certificados.

Para obtener más información sobre la autenticación y la comprobación de identidad mediante el uso de certificados, vea [Certificados digitales.](digital-certificates.md)

## <a name="integrity"></a>Integridad

Los datos enviados a través de un medio no seguro se pueden cambiar por accidente o a propósito. En el mundo real, los sellos se usan para proporcionar y demostrar integridad. Por ejemplo, una botella de cristal puede entrar en un empaquetado a prueba de manipulaciones que tiene un sello sin deshacer para demostrar que no se ha incluido nada en el paquete después de que el paquete abandonara el fabricante.

De la misma manera, un receptor de datos debe ser capaz de comprobar la identidad del remitente de los datos y asegurarse de que los datos recibidos son exactamente los datos enviados; es decir, que no se ha alterado. El establecimiento [*de la*](../secgloss/i-gly.md) integridad de los datos recibidos a menudo se realiza mediante el envío no solo de los datos originales, sino también de un mensaje de comprobación, denominado [*hash*](../secgloss/h-gly.md), sobre los datos. Tanto los datos como el mensaje de comprobación se pueden enviar con una [*firma digital*](../secgloss/d-gly.md) que demuestre el origen de ambos.

La integridad se proporciona en CryptoAPI mediante firmas [digitales](digital-signatures.md) y [hashes de datos.](data-hashes.md)

[*CryptoAPI admite*](../secgloss/c-gly.md) la integridad mediante el uso de funciones de mensaje para firmar datos y comprobar firmas digitales.

 

 

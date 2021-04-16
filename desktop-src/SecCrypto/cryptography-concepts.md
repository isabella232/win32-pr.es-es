---
description: 'Normalmente, la comunicación segura a través de redes no seguras implica tres áreas principales de preocupación: privacidad, autenticación e integridad.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Conceptos de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aad1528032c20c5492a98798f8a175ca331e462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666412"
---
# <a name="cryptography-concepts"></a>Conceptos de criptografía

Normalmente, la comunicación segura a través de redes no seguras implica tres áreas principales de preocupación: [privacidad](#privacy), [autenticación](#authentication)e [integridad](#integrity). Microsoft Cryptography API ([*CryptoAPI*](../secgloss/c-gly.md)) es un conjunto de funciones, interfaces y herramientas que las aplicaciones pueden usar para mejorar la confianza de la seguridad en estas áreas.

Además de la funcionalidad de privacidad, autenticación e integridad, [*CryptoAPI*](../secgloss/c-gly.md) también proporciona:

-   Codificación de mensajes en el formulario de [*notación de sintaxis abstracta uno*](../secgloss/a-gly.md) (ASN. 1).
-   Descodificando mensajes ASN. 1.
-   Administrar recopilaciones de [*certificados*](../secgloss/c-gly.md) en [*almacenes de certificados*](../secgloss/c-gly.md).
-   Trabajar con [*listas*](../secgloss/c-gly.md) de certificados de confianza y cadenas de certificados para comprobar la validez de los certificados.

## <a name="privacy"></a>Privacidad

Para lograr la privacidad, los usuarios deben evitar que cualquier persona excepto el destinatario previsto lea un mensaje. La mejora de la probabilidad de privacidad normalmente implica el uso de alguna forma de [*Criptografía*](../secgloss/c-gly.md). Las técnicas criptográficas se utilizan para cifrar mensajes (codificar) antes de que los mensajes se almacenen o se transmitan.

El cifrado de datos transforma el [*texto sin formato*](../secgloss/p-gly.md) en [*texto cifrado*](../secgloss/c-gly.md). Los datos que se van a cifrar pueden ser texto [*ASCII*](../secgloss/a-gly.md) , un archivo de base de datos o cualquier otro dato. En esta documentación, el término [*mensaje*](../secgloss/m-gly.md) se usa para hacer referencia a cualquier dato, el texto sin formato hace referencia a los datos que no se han cifrado y el *texto* cifrado hace referencia a los datos que se han cifrado. Un buen sistema de cifrado de datos dificulta la transformación de los datos cifrados en texto no cifrado sin una clave secreta.

Los datos cifrados se pueden almacenar en medios no seguros o transmitirse a través de una red no segura. Posteriormente, los datos se pueden descifrar en su forma original. Este proceso se muestra en la siguiente ilustración.

![ayuda para conservar la privacidad en todo el cifrado y descifrado](images/capi01.png)

Cuando se cifran los datos, el mensaje y una clave de [*cifrado*](../secgloss/e-gly.md) se pasan al algoritmo de cifrado. Para descifrar los datos, el texto cifrado y una clave de [*descifrado*](../secgloss/d-gly.md) se pasan al algoritmo de descifrado. El cifrado y el descifrado se pueden realizar mediante una clave única en un proceso denominado cifrado simétrico.

Las claves usadas para descifrar un mensaje deben ser secretas y seguras, y deben transmitirse a otros usuarios mediante técnicas de mejora de la seguridad. Esto se describe con más detalle en [cifrado y descifrado de datos](data-encryption-and-decryption.md). El principal desafío es restringir correctamente el acceso a la clave de descifrado, ya que cualquier persona que lo posea podrá descifrar todos los mensajes cifrados con su clave de cifrado correspondiente.

Para abordar los objetivos indicados de privacidad, los desarrolladores pueden usar [*CryptoAPI*](../secgloss/c-gly.md) para cifrar y firmar digitalmente los datos de manera flexible, al tiempo que ayuda a proporcionar protección para los datos de clave privada confidenciales del usuario.

[*CryptoAPI*](../secgloss/c-gly.md) proporciona las siguientes áreas de funcionalidad para realizar las tareas de cifrado y descifrado, firma de mensajes y almacenamiento de claves:

-   [Funciones criptográficas base](cryptography-functions.md)
-   [Funciones de mensaje simplificadas](cryptography-functions.md)
-   [Funciones de mensajes de bajo nivel](cryptography-functions.md)

## <a name="authentication"></a>Autenticación

Las comunicaciones seguras requieren que las personas que se comunican conozcan la identidad de los usuarios con los que se comunican. La autenticación es el proceso de comprobar la identidad de una persona o entidad.

Por ejemplo, en la vida diaria, la documentación física, que a menudo se denomina credenciales, se usa para comprobar la identidad de una persona. Cuando se cobrada una comprobación, la persona que realice la comprobación puede solicitar ver la licencia de un controlador. La licencia del controlador es un documento físico que aumenta la confianza del comerciante en la identidad de la persona que está en el efectivo de la comprobación. En este caso, la persona que se ponga en contacto con la comprobación confía en que el estado que emite la licencia comprobó adecuadamente la identidad del titular de la licencia.

Los pasaportes proporcionan otro ejemplo. Un funcionario aduanero examina un pasaporte y lo acepta como prueba de que una persona es quien dice ser. El funcionario confía en que el Gobierno ha realizado un trabajo adecuado para identificar al titular de Passport antes de emitir el pasaporte. En ambos ejemplos, existe un nivel de confianza en el emisor del documento físico.

La autenticación también implica asegurarse de que los datos recibidos son los datos que se enviaron. Si la entidad A envía un mensaje a la entidad B, la entidad B debe ser capaz de demostrar que el mensaje recibido fue el mensaje que la parte A ha enviado, y no un mensaje que se ha sustituido por ese mensaje. Para proporcionar esta forma de autenticación, [*CryptoAPI*](../secgloss/c-gly.md) proporciona funciones para firmar datos y comprobar firmas mediante pares de claves pública y privada.

Dado que las comunicaciones a través de una red de equipos tienen lugar sin contacto físico entre los comunicadores, comprobar la identidad depende a menudo de una credencial que se puede enviar y recibir a través de una red. Este tipo de credenciales debe ser emitido por un emisor de confianza de credenciales. Los certificados digitales, conocidos normalmente como certificados, son solo tales credenciales. Son una forma de comprobar la identidad y conseguir la autenticación en una red de equipos.

Un certificado digital es una credencial emitida por una organización de confianza o entidad denominada entidad de certificación (CA). Esta credencial contiene una clave pública (consulte los [pares de claves pública y privada](public-private-key-pairs.md)) y los datos que identifican el sujeto del certificado. Un certificado es emitido por una CA solo después de que la entidad de certificación haya comprobado la identidad del sujeto del certificado y haya confirmado que la clave pública incluida con el certificado pertenece a ese asunto.

La comunicación entre una entidad de certificación y un solicitante de certificado podría llevarla a cabo el solicitante físicamente que lleve la información necesaria, posiblemente almacenada en un disquete, a la CA. Sin embargo, la comunicación se realiza normalmente con un mensaje firmado enviado a través de una red. La CA suele usar una aplicación de confianza denominada servidor de certificados para emitir certificados.

[*CryptoAPI*](../secgloss/c-gly.md) admite la autenticación mediante el uso de certificados digitales, con funciones de codificación y descodificación de certificados, y con funciones de [*almacén de certificados*](../secgloss/c-gly.md) .

Para obtener más información acerca de la comprobación de identidades y la autenticación mediante el uso de certificados, consulte [certificados digitales](digital-certificates.md).

## <a name="integrity"></a>Integridad

Los datos enviados a través de un medio no seguro se pueden cambiar por accidente o a propósito. En el mundo real, se usan sellos para proporcionar y demostrar la integridad. Un frasco de aspirin, por ejemplo, puede estar en un paquete de prueba de alteración que tiene un sello sin romper para demostrar que no se colocó nada en el paquete después de que el paquete abandone el fabricante.

Del mismo modo, un receptor de datos debe ser capaz de comprobar la identidad del remitente de los datos y asegurarse de que los datos recibidos son exactamente los que se enviaron; es decir, que no se ha alterado. El establecimiento de la [*integridad*](../secgloss/i-gly.md) de los datos recibidos se suele realizar enviando no solo los datos originales sino también un mensaje de comprobación, denominado [*hash*](../secgloss/h-gly.md), sobre los datos. Tanto los datos como el mensaje de comprobación se pueden enviar con una [*firma digital*](../secgloss/d-gly.md) que demuestre el origen de ambos.

La integridad se proporciona en CryptoAPI mediante el uso de [firmas digitales](digital-signatures.md) y [hashes de datos](data-hashes.md).

[*CryptoAPI*](../secgloss/c-gly.md) admite la integridad mediante el uso de funciones de mensaje para firmar datos y comprobar firmas digitales.

 

 

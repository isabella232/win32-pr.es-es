---
description: Certificate Services es una base para la infraestructura de clave pública (PKI) que proporciona los medios para proteger y autenticar la información.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Certificados y claves públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d5f1996549184b8c56388bdb3ae8395eee077bca31b03e074f4dda8568805b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770625"
---
# <a name="certificates-and-public-keys"></a>Certificados y claves públicas

Certificate Services es una base para la infraestructura de clave pública (PKI) que proporciona los medios para proteger y autenticar la información. La relación entre un titular de certificados, la identidad del [](../secgloss/p-gly.md) titular del certificado y la clave pública del titular del certificado es una parte fundamental de la PKI. Esta infraestructura se conste de las siguientes partes:

-   [Par de claves pública y privada](#the-publicprivate-key-pair)
-   [La solicitud de certificado](#the-certificate-request)
-   [La entidad de certificación](#the-certification-authority)
-   [El certificado](#the-certificate-request)
-   [Lista de revocación de certificados](#the-certificate-revocation-list)
-   [La clave pública usada para el cifrado](#your-public-key-used-for-encryption)
-   [La clave pública usada para la comprobación de firmas](#your-public-key-used-for-signature-verification)
-   [Rol servicios de certificados de Microsoft](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>Par de claves pública y privada

PKI requiere el uso de [*pares de claves pública y privada.*](../secgloss/p-gly.md) Las matemáticas de los pares de claves públicas y privadas están fuera del ámbito de esta documentación, pero es importante tener en cuenta la relación funcional entre una clave pública y una clave privada. Los algoritmos [*criptográficos*](../secgloss/c-gly.md) PKI usan la clave pública del [](../secgloss/p-gly.md) receptor de un mensaje cifrado para cifrar los datos y la clave privada relacionada y solo la clave privada relacionada para descifrar el mensaje cifrado. [](../secgloss/p-gly.md)

De forma similar, se [*crea una*](../secgloss/d-gly.md) firma digital del contenido, que se describe con más detalle a continuación, con la clave privada del firmante. La clave pública correspondiente, que está disponible para todos los usuarios, se usa para comprobar esta firma. Se debe mantener la confidencialidad de la clave privada porque el marco se desmorona después de que la clave privada esté en peligro.

Dado el tiempo y los recursos suficientes, se puede poner en peligro un par de claves pública y privada, es decir, se puede detectar la clave privada. Cuanto más larga sea la clave, más difícil es usar la fuerza bruta para detectar la clave privada. En la práctica, se pueden usar claves suficientemente seguras para que sea inviable determinar la clave privada de forma oportuna, lo que convierte a la infraestructura de clave pública en un mecanismo de seguridad viable.

Una clave privada se puede almacenar, en formato protegido, en un disco, en cuyo caso solo se puede usar con ese equipo específico a menos que se haya movido físicamente a otro equipo. Una alternativa es tener una clave en una tarjeta inteligente que se pueda usar en otro equipo siempre que tenga un lector de tarjeta inteligente y software de soporte técnico.

La clave pública, pero no la clave privada, del sujeto de un certificado digital se incluye como parte de la solicitud [*de certificado*](../secgloss/c-gly.md). (Por lo tanto, debe existir un par de claves pública y privada antes de realizar la solicitud de certificado). Esa clave pública pasa a formar parte del certificado emitido.

## <a name="the-certificate-request"></a>La solicitud de certificado

Antes de emitir un certificado, se [*debe generar*](../secgloss/c-gly.md) una solicitud de certificado. Esta solicitud se aplica a una entidad, por ejemplo, un usuario final, un equipo o una aplicación. Para obtener información, suponga que la entidad es usted mismo. Los detalles de la identidad se incluyen en la solicitud de certificado. Una vez generada la solicitud, se envía a una entidad [*de certificación*](../secgloss/c-gly.md) (CA). A continuación, la entidad de certificación usa la información de identidad para determinar si la solicitud cumple los criterios de la entidad de certificación para emitir un certificado. Si la entidad de certificación aprueba la solicitud, le emite un certificado, como la entidad denominada en la solicitud.

## <a name="the-certification-authority"></a>La entidad de certificación

Antes de emitir el certificado, la entidad de certificación comprueba su identidad. Cuando se emite el certificado, la identidad se enlaza al certificado, que contiene la clave pública. El certificado también contiene la firma digital de la entidad de certificación (que puede comprobar cualquier persona que reciba el certificado).

Dado que el certificado contiene la identidad de la CA emisora, un interesado que confíe en esta CA puede extender esa confianza al certificado. La emisión de un certificado no establece confianza, sino que transfiere la confianza. Si el consumidor de certificados no confía en la CA emisora, no confiará (o al menos no debería) en el certificado.

Una cadena de certificados firmados también permite transferir la confianza a otras CA. Esto permite a las partes que usan diferentes CA seguir siendo capaces de confiar en los certificados (siempre que haya una ENTIDAD de certificación común en la cadena, es decir, una CA de confianza para ambas partes).

## <a name="the-certificate"></a>El certificado

Además de la clave pública y la identidad de la CA emisora, el certificado emitido contiene información sobre los propósitos de la clave y el certificado. Además, incluye la ruta de acceso a la lista de certificados revocados de la entidad de certificación y especifica el período de validez del certificado (fechas de inicio y finalización).

Suponiendo que el consumidor de certificados confíe en la CA emisora para el certificado, el consumidor de certificados debe determinar si el certificado sigue siendo válido comparando las fechas inicial y final del certificado con la hora actual y comprobando que el certificado no está en la lista de certificados revocados de la entidad de certificación.

## <a name="the-certificate-revocation-list"></a>Lista de revocación de certificados

Suponiendo que el certificado se usa en un período de tiempo válido y el consumidor del certificado confía en la CA emisora, hay un elemento más para que el consumidor de certificados compruebe antes de usar el certificado: la lista de [*revocación*](../secgloss/c-gly.md) de certificados (CRL). El consumidor de certificados comprueba la CRL de la entidad de certificación (la ruta de acceso a la que se incluye como una extensión en el certificado) para asegurarse de que el certificado no está en la lista de certificados que se han revocado. Existen CRL porque hay ocasiones en las que un certificado no ha expirado, pero ya no se puede confiar en él. Periódicamente, la CA publicará una CRL actualizada. Los consumidores de certificados son responsables de comparar los certificados con la CRL actual antes de considerar el certificado de confianza.

## <a name="your-public-key-used-for-encryption"></a>La clave pública usada para el cifrado

Si un remitente desea cifrar un mensaje antes de enviarlo, el remitente recupera primero el certificado. Después de que el remitente determine que la entidad de certificación es de confianza y que el certificado es válido y [](../secgloss/p-gly.md) no revocado, el remitente usa la clave pública (recuerde que forma parte del certificado) con algoritmos criptográficos para cifrar el mensaje de texto no cifrado en texto [*cifrado*](../secgloss/c-gly.md). Cuando reciba el texto cifrado, usará la clave privada para descifrar el texto cifrado.

Si un tercero intercepta el mensaje de correo electrónico de texto cifrado, el tercero no podrá descifrarlo sin acceso a [*la clave privada.*](../secgloss/p-gly.md)

Tenga en cuenta que la mayor parte de las actividades enumeradas aquí se controlan mediante software, no directamente por el usuario.

## <a name="your-public-key-used-for-signature-verification"></a>La clave pública usada para la comprobación de firmas

Una [*firma digital*](../secgloss/d-gly.md) se usa como confirmación de que no se ha modificado un mensaje y como confirmación de la identidad del remitente del mensaje. Esta firma digital depende de la clave privada y del contenido del mensaje. Con el mensaje como entrada y la clave privada, los algoritmos criptográficos crean la firma digital. El proceso de firma no cambia el contenido del mensaje. Un destinatario puede usar la clave pública (después de comprobar la validez del certificado, la entidad de certificación emisora y el estado de revocación) para determinar si la firma corresponde al contenido del mensaje y determinar si el mensaje lo envió usted.

Si un tercero intercepta el mensaje previsto, lo modifica (incluso ligeramente) y lo reenvía y la firma original al destinatario, el destinatario, tras el examen del mensaje y la firma, podrá determinar que el mensaje es sospechoso. Del mismo modo, si un tercero crea un mensaje y lo envía con una firma digital falsa bajo la apariencia de que se originó en usted, el destinatario podrá usar la clave pública para determinar que el mensaje y la firma no se corresponden entre sí.

[*Las firmas digitales también*](../secgloss/n-gly.md) admiten la no reesudiación. Si el remitente de un mensaje firmado deniega el envío del mensaje, el destinatario puede usar la firma para desmentir esa notificación.

Tenga en cuenta que la mayor parte de las actividades enumeradas aquí también se controlan mediante software, no directamente por el usuario.

## <a name="microsoft-certificate-services-role"></a>Rol servicios de certificados de Microsoft

Microsoft Certificate Services tiene el rol de emitir certificados o denegar solicitudes de certificados, tal y como se indica en los módulos de directivas, que son responsables de garantizar la identidad del solicitante de certificados. Servicios de certificados también proporciona la capacidad de revocar un certificado, así como de publicar la CRL. Los servicios de certificados también pueden distribuir centralmente (por ejemplo, a un servicio de directorio) certificados emitidos. La capacidad de emitir, distribuir, revocar y administrar certificados, junto con la publicación de CRL, proporciona las funcionalidades necesarias para la infraestructura de clave pública.

 

 

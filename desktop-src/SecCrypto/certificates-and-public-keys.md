---
description: Los servicios de Certificate Server son una base para la infraestructura de clave pública (PKI) que proporciona los medios para proteger y autenticar la información.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Certificados y claves públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e01993673fe16c8401368ffaa7e8815c450dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908335"
---
# <a name="certificates-and-public-keys"></a>Certificados y claves públicas

Los servicios de Certificate Server son una base para la infraestructura de clave pública (PKI) que proporciona los medios para proteger y autenticar la información. La relación entre un titular del certificado, la identidad del titular del certificado y la [*clave pública*](../secgloss/p-gly.md) del titular del certificado es una parte crítica de la PKI. Esta infraestructura se compone de las siguientes partes:

-   [El par de claves pública y privada](#the-publicprivate-key-pair)
-   [La solicitud de certificado](#the-certificate-request)
-   [La entidad de certificación](#the-certification-authority)
-   [El certificado](#the-certificate-request)
-   [Lista de revocación de certificados](#the-certificate-revocation-list)
-   [La clave pública que se usa para el cifrado](#your-public-key-used-for-encryption)
-   [La clave pública que se usa para la comprobación de firmas](#your-public-key-used-for-signature-verification)
-   [Rol servicios de certificados de Microsoft](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>El par de claves pública y privada

PKI requiere el uso de [*pares de claves pública y privada*](../secgloss/p-gly.md). La matemática de pares de claves pública y privada está fuera del ámbito de esta documentación, pero es importante tener en cuenta la relación funcional entre una clave pública y una privada. Los [*algoritmos criptográficos*](../secgloss/c-gly.md) de PKI usan la [*clave pública*](../secgloss/p-gly.md) del receptor de un mensaje cifrado para cifrar los datos, y la [*clave privada*](../secgloss/p-gly.md) relacionada y solo la clave privada relacionada para descifrar el mensaje cifrado.

Del mismo modo, se crea una [*firma digital*](../secgloss/d-gly.md) del contenido, que se describe con más detalle a continuación, con la clave privada del firmante. La clave pública correspondiente, que está disponible para todos, se usa para comprobar esta firma. Se debe mantener la confidencialidad de la clave privada, ya que el marco de trabajo queda separado después de que la clave privada se haya puesto en peligro.

Dado tiempo y recursos suficientes, se puede poner en peligro un par de claves pública y privada, es decir, se puede detectar la clave privada. Cuanto más larga sea la clave, más difícil será usar la fuerza bruta para detectar la clave privada. En la práctica, se pueden usar claves suficientemente seguras para que no sea factible determinar la clave privada de manera oportuna, lo que hace que la infraestructura de clave pública sea un mecanismo de seguridad viable.

Se puede almacenar una clave privada, en formato protegido, en un disco, en cuyo caso solo se puede usar con ese equipo específico a menos que se mueva físicamente a otro equipo. Una alternativa consiste en tener una clave en una tarjeta inteligente que se pueda usar en otro equipo, siempre que tenga un lector de tarjetas inteligentes y software de soporte.

La clave pública, pero no la clave privada, del firmante de un certificado digital se incluye como parte de la [*solicitud de certificado*](../secgloss/c-gly.md). (Por lo tanto, un par de claves pública y privada debe existir antes de efectuar la solicitud de certificado). Esa clave pública se convierte en parte del certificado emitido.

## <a name="the-certificate-request"></a>La solicitud de certificado

Antes de emitir un certificado, debe generarse una [*solicitud de certificado*](../secgloss/c-gly.md) . Esta solicitud se aplica a una entidad, por ejemplo, un usuario final, un equipo o una aplicación. En el debate, supongamos que la entidad es usted mismo. Los detalles de su identidad se incluyen en la solicitud de certificado. Una vez generada la solicitud, se envía a una [*entidad de certificación*](../secgloss/c-gly.md) (CA). A continuación, la CA usa la información de identidad para determinar si la solicitud cumple los criterios de la CA para emitir un certificado. Si la entidad de certificación aprueba la solicitud, emite un certificado, como la entidad denominada en la solicitud.

## <a name="the-certification-authority"></a>La entidad de certificación

Antes de emitir el certificado, la entidad de certificación comprueba la identidad. Cuando se emite el certificado, su identidad se enlaza al certificado, que contiene la clave pública. El certificado también contiene la firma digital de la CA (que puede ser comprobada por cualquiera que reciba el certificado).

Dado que el certificado contiene la identidad de la CA emisora, una entidad interesada que confíe en esta entidad de certificación puede extender dicha confianza al certificado. La emisión de un certificado no establece confianza, pero transfiere la confianza. Si el consumidor del certificado no confía en la CA emisora, no podrá confiar (o al menos) en el certificado.

Una cadena de certificados firmados permite transferir también la confianza a otras CA. Esto permite que las partes que usan diferentes CA sigan pudiendo confiar en los certificados (siempre que haya una CA común en la cadena, es decir, una CA de confianza para ambas partes).

## <a name="the-certificate"></a>El certificado

Además de la clave pública y la identidad de la CA emisora, el certificado emitido contiene información sobre los propósitos de la clave y el certificado. Además, incluye la ruta de acceso a la lista de certificados revocados de la entidad de certificación y especifica el período de validez del certificado (fechas de inicio y finalización).

Suponiendo que el certificado del consumidor confía en la CA emisora del certificado, el consumidor del certificado debe determinar si el certificado sigue siendo válido comparando las fechas de inicio y finalización del certificado con la hora actual y comprobando que el certificado no se encuentra en la lista de certificados revocados de la entidad de certificación.

## <a name="the-certificate-revocation-list"></a>Lista de revocación de certificados

Suponiendo que el certificado se esté usando en un período de tiempo válido y que el consumidor del certificado confíe en la CA emisora, hay un elemento más para que el consumidor del certificado Compruebe antes de usar el certificado: la [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL). El consumidor del certificado comprueba la CRL de la entidad de certificación (la ruta de acceso a la que se incluye como extensión en el certificado) para asegurarse de que el certificado no está en la lista de certificados que se han revocado. Existen listas CRL porque hay veces en que un certificado no ha expirado, pero ya no puede ser de confianza. De forma periódica, la CA publicará una CRL actualizada. Los consumidores de certificados son responsables de comparar los certificados con la CRL actual antes de considerar que el certificado es de confianza.

## <a name="your-public-key-used-for-encryption"></a>La clave pública que se usa para el cifrado

Si un remitente desea cifrar un mensaje antes de enviarlo, el remitente recupera primero el certificado. Una vez que el remitente determina que la CA es de confianza y el certificado es válido y no está revocado, el remitente usa la clave pública (Recuerde que forma parte del certificado) con algoritmos criptográficos para cifrar el mensaje de [*texto simple*](../secgloss/p-gly.md) en [*texto*](../secgloss/c-gly.md)cifrado. Cuando reciba el texto cifrado, use la clave privada para descifrar el texto cifrado.

Si un tercero intercepta el mensaje de correo electrónico cifrado, el tercero no podrá descifrarlo sin tener acceso a la [*clave privada*](../secgloss/p-gly.md).

Tenga en cuenta que la mayor parte de las actividades que se enumeran aquí se administran mediante software, no directamente por el usuario.

## <a name="your-public-key-used-for-signature-verification"></a>La clave pública que se usa para la comprobación de firmas

Una [*firma digital*](../secgloss/d-gly.md) se utiliza como confirmación de que un mensaje no se ha modificado y como confirmación de la identidad del remitente del mensaje. Esta firma digital depende de la clave privada y el contenido del mensaje. Con el mensaje como entrada y su clave privada, los algoritmos criptográficos crean la firma digital. El proceso de firma no cambia el contenido del mensaje. Un destinatario puede usar su clave pública (después de comprobar la validez del certificado, la entidad emisora de certificados y el estado de revocación) para determinar si la firma se corresponde con el contenido del mensaje y determinar si el mensaje se envió por usted.

Si un tercero intercepta el mensaje previsto, lo modifica (incluso ligeramente) y lo reenvía y la firma original al destinatario, el destinatario, al examinar el mensaje y la firma, podrá determinar que el mensaje es sospechoso. Del mismo modo, si un tercero crea un mensaje y lo envía con una firma digital ficticia en el caso de que se origine, el destinatario podrá usar su clave pública para determinar que el mensaje y la firma no se correspondan entre sí.

El no [*rechazo*](../secgloss/n-gly.md) también es compatible con las firmas digitales. Si el remitente de un mensaje firmado deniega el envío del mensaje, el destinatario puede usar la firma para refute esa demanda.

Tenga en cuenta que la mayor parte de las actividades que se enumeran aquí también se controlan mediante software, no directamente por el usuario.

## <a name="microsoft-certificate-services-role"></a>Rol servicios de certificados de Microsoft

Los servicios de Certificate Server de Microsoft tienen el rol de emitir certificados o denegar solicitudes de certificados, según lo indicado por los módulos de directivas, que son responsables de garantizar la identidad del solicitante de certificados. Los servicios de Certificate Server también proporcionan la capacidad de revocar un certificado, así como publicar la CRL. Los servicios de Certificate Server también pueden distribuir de forma centralizada (por ejemplo, a un servicio de directorio) los certificados emitidos. La capacidad de emitir, distribuir, revocar y administrar certificados, junto con la publicación de CRL, proporciona las capacidades necesarias para la infraestructura de clave pública.

 

 

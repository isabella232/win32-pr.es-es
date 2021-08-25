---
description: Cómo proporcionan los certificados digitales comunicaciones seguras y cómo usar CryptoAPI para usar y administrar esos certificados.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Certificados digitales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f2df1a529d94fa5a04385c7f91f5aefbb40c0488ef0c5c484fe98c3874358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875305"
---
# <a name="digital-certificates"></a>Certificados digitales

La autenticación es fundamental para proteger las comunicaciones. Los usuarios deben poder demostrar su identidad a aquéllos con los que se comunican y deben ser capaces de comprobar la identidad de los otros. La autenticación de la identidad en una red es compleja porque las partes que se comunican no se conocen físicamente. Esto puede permitir que una persona desconocida intercepte mensajes o se haga pasar por otra persona o entidad. Se debe trabajar con un método para mantener el nivel de confianza necesario dentro del proceso de comunicación.

El [*certificado digital*](../secgloss/c-gly.md) es una credencial común que proporciona un medio para comprobar la identidad. En esta sección se proporciona información general sobre cómo los certificados proporcionan comunicaciones seguras y cómo usar CryptoAPI para usar y administrar esos certificados.

Un certificado es un conjunto de datos que identifica una entidad. Una organización de confianza asigna un certificado a un individuo o a una entidad que asocia una clave pública a la persona. La persona o entidad a la que se emite un certificado se denomina sujeto de ese certificado. La organización de confianza que emite el certificado es una entidad [*de certificación*](../secgloss/c-gly.md) (CA) y se conoce como emisor del certificado. Una CA de confianza solo emitirá un certificado después de comprobar la identidad del sujeto del certificado.

Los certificados usan técnicas criptográficas para solucionar el problema de la falta de contacto físico entre los que se comunican. El uso de estas técnicas limita la posibilidad de que una persona no ética intercepte, altere o falsee mensajes. Estas técnicas criptográficas dificultan la modificación de los certificados. Por lo tanto, es difícil para una entidad suplantar a otra persona.

Los datos de un certificado incluyen la clave criptográfica pública del par de claves pública y privada del sujeto [*del certificado.*](../secgloss/p-gly.md) El destinatario del mensaje solo puede recuperar un mensaje firmado con la clave privada de su remitente mediante la clave pública del remitente. Esta clave se puede encontrar en una copia del certificado del remitente. La recuperación de una firma con una [*clave pública*](../secgloss/p-gly.md) de un certificado demuestra que la firma se produjo mediante la clave privada del [*firmante del certificado.*](../secgloss/p-gly.md) Si el remitente ha estado atento y ha mantenido el secreto de clave privada, el receptor puede estar seguro de la identidad del remitente del mensaje.

En una red, a menudo hay una aplicación de confianza conocida como servidor [*de certificados*](../secgloss/c-gly.md). Una CA que se ejecuta en un equipo seguro administra el servidor de certificados. Esta aplicación tiene acceso a la clave pública de todos sus clientes. Los servidores de certificados dispensan mensajes conocidos como certificados, cada uno de los cuales contiene la clave pública de uno de sus usuarios cliente. Cada certificado se firma con la clave privada de la entidad de certificación. Por lo tanto, el receptor de este tipo de certificado puede comprobar que una entidad de certificación especificada lo ha enviado.

Los certificados digitales también incluyen extensiones y propiedades extendidas que proporcionan información adicional sobre el asunto del certificado, como la dirección de correo electrónico del sujeto y las actividades que el sujeto del certificado puede realizar.

 

 

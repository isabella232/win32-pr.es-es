---
description: Proceso para descodificar los datos firmados.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Descodificar datos firmados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666405"
---
# <a name="decoding-signed-data"></a>Descodificar datos firmados

El siguiente proceso general descodifica un tipo de [*datos con signo*](../secgloss/s-gly.md) .

**Para descodificar un mensaje firmado**

1.  Obtiene un puntero al objeto binario codificado.
2.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.
3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se van a descodificar. Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 2 y los tipos de parámetro adecuados para tener acceso a los datos descodificados. Por ejemplo, pase \_ el parámetro de contenido CMSG \_ para obtener un puntero al contenido descodificado.

En el siguiente proceso general se comprueba la firma de un mensaje con firma descodificado.

**Para comprobar la firma de un mensaje descodificado firmado**

1.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el parámetro de información del certificado del firmante CMSG y el identificador de mensaje \_ \_ \_ \_ para obtener [**la \_ información del certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmante del mensaje.
2.  Llame a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir un almacén temporal que se inicializa con los certificados del mensaje.
3.  Llame a [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) para obtener la información del [**certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmante de los certificados incluidos en el mensaje.
4.  Llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), pasando CMSG \_ Ctrl \_ Verify \_ Signature para comprobar las firmas.
5.  Llame a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

El resultado de estos procedimientos es que se comprueba la firma y se recupera un puntero al contenido del mensaje descodificado obtenido en el paso 4 del procedimiento para descodificar un mensaje firmado.

Para obtener información detallada sobre la codificación en C, vea [ejemplo de programa c: firma, codificación, descodificación y comprobación de un mensaje](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

 

 

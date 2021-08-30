---
description: Proceso para descodificar datos firmados.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Decoding Signed Data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3466736f6c8aab36184c02b918625a609a83c78c6f0142d3201d4c264d67441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875685"
---
# <a name="decoding-signed-data"></a>Decoding Signed Data

El siguiente proceso general descodifica un tipo [*de datos firmado.*](../secgloss/s-gly.md)

**Para descodificar un mensaje firmado**

1.  Obtenga un puntero al BLOB codificado.
2.  Llame [**a CryptMsgOpenToDecode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)pase los argumentos necesarios.
3.  Llame [**a CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se descodificarán. Esto hace que se tome las acciones adecuadas en el mensaje, en función del tipo de mensaje.
4.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador recuperado en el paso 2 y los tipos de parámetro adecuados para acceder a los datos descodificados. Por ejemplo, pase CONTENT PARAM de CMSG \_ para obtener un puntero al contenido \_ descodificado.

El siguiente proceso general comprueba la firma de un mensaje descodificado y firmado.

**Para comprobar la firma de un mensaje descodificado y firmado**

1.  Llame [**a CryptMsgGetParam,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)pasando el identificador del mensaje y CMSG SIGNER CERT INFO PARAM para obtener la información del CERTIFICADO del \_ \_ \_ \_ firmante del [**\_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) mensaje.
2.  Llame [**a CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) para abrir un almacén temporal que se inicializa con los certificados del mensaje.
3.  Llame [**a CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) para obtener la información del [**CERTIFICADO \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) del firmante de los certificados incluidos en el mensaje.
4.  Llame [**a CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)y pase CMSG \_ CTRL VERIFY SIGNATURE para comprobar las \_ \_ firmas.
5.  Llame [**a CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.

El resultado de estos procedimientos es que se comprueba la firma y se recupera un puntero al contenido del mensaje descodificado obtenido en el paso 4 del procedimiento para descodificar un mensaje firmado.

Para obtener detalles de codificación de C, vea [Programa de C de ejemplo: firma, codificación, codificación](example-c-program-signing-encoding-decoding-and-verifying-a-message.md)y comprobación de un mensaje .

 

 

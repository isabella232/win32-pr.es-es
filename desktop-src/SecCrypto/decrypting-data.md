---
description: Presenta los pasos necesarios para descifrar un mensaje cifrado.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Descifrar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361630"
---
# <a name="decrypting-data"></a>Descifrar datos

En esta sección se presentan los pasos para descifrar un mensaje cifrado.

**Para descifrar un mensaje cifrado**

1.  Obtiene un puntero al mensaje con doble cifrado.
2.  Abra un almacén de certificados.
3.  En el mensaje, recupere el identificador de destinatario (My ID).
4.  Use el identificador de destinatario para recuperar el certificado.
5.  Obtiene la clave privada del certificado.
6.  Use la clave privada para descifrar la clave simétrica (sesión).
7.  Recupere el algoritmo de cifrado del mensaje.
8.  Descifre los datos mediante la clave de sesión descifrada y el algoritmo de cifrado.

[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) realiza todas las tareas para descifrar un mensaje. sin embargo, todavía es necesario inicializar las estructuras y otros datos.

**Para descifrar datos mediante CryptDecryptMessage**

1.  Obtiene un puntero al BLOB cifrado.
2.  Abra un almacén de certificados.
3.  Cree una matriz de almacén de certificados.
4.  Inicialice el [**\_ mensaje del descifrado del cifrado \_ \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) la estructura.
5.  Llame a [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para descifrar los datos contenidos en el mensaje.

[Programa C de ejemplo: el uso de CryptEncryptMessage y CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa el procedimiento que se acaba de presentar. Los comentarios muestran los elementos de código que realizan cada paso del procedimiento. Para obtener más información sobre la función, vea [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)y para obtener más información sobre la estructura de datos, vea Crypt [**\_ descrypt \_ Message \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 




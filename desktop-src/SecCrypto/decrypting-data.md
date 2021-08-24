---
description: Presenta los pasos para descifrar un mensaje cifrado.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Descifrar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600903d7a3060c83cd7cd0a85e92f96efe4fb0cfa30c2936c5546f71138b6854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875695"
---
# <a name="decrypting-data"></a>Descifrar datos

En esta sección se presentan los pasos para descifrar un mensaje cifrado.

**Para descifrar un mensaje cifrado**

1.  Obtenga un puntero al mensaje con sobre digital.
2.  Abra un almacén de certificados.
3.  En el mensaje, recupere el identificador de destinatario (Mi identificador).
4.  Use el identificador de destinatario para recuperar el certificado.
5.  Obtenga la clave privada del certificado.
6.  Use la clave privada para descifrar la clave simétrica (sesión).
7.  Recupere el algoritmo de cifrado del mensaje.
8.  Con la clave de sesión descifrada y el algoritmo de cifrado, descifre los datos.

[**CryptDecryptMessage realiza**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) todas las tareas para descifrar un mensaje; sin embargo, la inicialización de estructuras y otros datos sigue siendo necesaria.

**Para descifrar datos mediante CryptDecryptMessage**

1.  Obtenga un puntero al BLOB cifrado.
2.  Abra un almacén de certificados.
3.  Cree una matriz de almacén de certificados.
4.  Inicialice la [**estructura CRYPT \_ DECRYPT MESSAGE \_ \_ PARA.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para)
5.  Llame [**a CryptDecryptMessage para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) descifrar los datos contenidos en el mensaje.

[Programa C de ejemplo: el uso de CryptEncryptMessage y CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa el procedimiento que se acaba de presentar. Los comentarios muestran qué elementos de código logran cada paso del procedimiento. Para obtener más información sobre la función, vea [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)y, para obtener más información sobre la estructura de datos, vea [**CRYPT \_ DECRYPT MESSAGE \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).

 

 




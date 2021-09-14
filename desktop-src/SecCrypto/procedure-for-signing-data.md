---
description: Muestra la relación entre esos parámetros de función que apuntan a estructuras o matrices y sus datos inicializados.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procedimiento para firmar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170894"
---
# <a name="procedure-for-signing-data"></a>Procedimiento para firmar datos

Una sola función, [**CryptSignMessage,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)realiza todas las tareas enumeradas en [Creación de un mensaje firmado.](creating-a-signed-message.md) Sin embargo, la inicialización de estructuras y otros datos sigue siendo necesaria. En la ilustración siguiente se muestra la relación entre los parámetros de función que apuntan a estructuras o matrices y sus datos inicializados. En la ilustración solo se muestran los parámetros de función y los miembros de estructura que se derivan de otras estructuras o funciones. El resto de los parámetros son inicializaciones sencillas.

![mapa de inicialización para una llamada a cryptsignmessage](images/crypsign.png)

**Para firmar datos mediante CryptSignMessage**

1.  Obtenga un puntero a los datos que se va a firmar.
2.  Asigne el puntero a los datos para indexar cero de una matriz "data to be signed".
3.  Obtenga un identificador para el proveedor de servicios criptográficos.
4.  Abra un [*almacén de certificados*](../secgloss/c-gly.md) que contenga el certificado del firmante.
5.  Obtenga una dirección al certificado del firmante.
6.  Asigne la dirección del certificado al índice cero de la *matriz MsgCert.*
7.  Asigne las direcciones de cualquier otro certificado que se incluirá con el mensaje a la *matriz MsgCert.*
8.  Inicialice [**la estructura CRYPT ALGORITHM \_ \_ IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) e inicialice el **miembro pszObjId** en el algoritmo hash deseado y los demás miembros según corresponda.
9.  Inicialice la estructura [**CRYPT \_ SIGN MESSAGE \_ \_ PARA,**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) inicializando el miembro **pSigningCert** en la dirección del certificado del firmante, el miembro de matriz **MsgCert** en la dirección de los certificados del firmante y otros, el miembro **HashAlgorithm** en la dirección de la estructura [**CRYPT ALGORITHM \_ \_ IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) y los demás miembros según corresponda.
10. Llame a la función [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) y pase la estructura [**CRYPT \_ SIGN MESSAGE \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) para el parámetro *pSignPara,* la dirección de la matriz "data to be signed" para el *parámetro rgpbToBeSigned,* una dirección para el parámetro de salida *pbSignedBlob* y los valores de los demás parámetros según corresponda.

 

 

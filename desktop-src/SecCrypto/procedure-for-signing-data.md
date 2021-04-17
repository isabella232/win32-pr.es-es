---
description: Muestra la relación entre los parámetros de función que apuntan a estructuras o matrices y sus datos inicializados.
ms.assetid: 89caf4d3-727f-472b-9a09-e81b4ff4d127
title: Procedimiento para firmar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba289928ab39c690e1c44bdbf65c77c18b7edab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687593"
---
# <a name="procedure-for-signing-data"></a>Procedimiento para firmar datos

Una sola función, [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage), realiza todas las tareas enumeradas en [crear un mensaje firmado](creating-a-signed-message.md). Sin embargo, todavía es necesario inicializar las estructuras y otros datos. En la ilustración siguiente se muestra la relación entre los parámetros de función que apuntan a estructuras o matrices y sus datos inicializados. En la ilustración solo se muestran los parámetros de función y los miembros de estructura que se derivan de otras estructuras o funciones. El resto de los parámetros son inicializaciones sencillas.

![asignación de inicialización para una llamada a cryptsignmessage](images/crypsign.png)

**Para firmar datos mediante CryptSignMessage**

1.  Obtiene un puntero a los datos que se van a firmar.
2.  Asigne el puntero a los datos para indizar cero de una matriz "datos que se van a firmar".
3.  Obtiene un identificador para el proveedor de servicios criptográficos.
4.  Abra un [*almacén de certificados*](../secgloss/c-gly.md) que contenga el certificado del firmante.
5.  Obtenga una dirección para el certificado del firmante.
6.  Asigne la dirección del certificado al índice cero de la matriz *MsgCert* .
7.  Asigne las direcciones de cualquier otro certificado que se va a incluir con el mensaje en la matriz *MsgCert* .
8.  Inicialice la estructura del [**\_ \_ identificador del algoritmo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) , inicializando el miembro **pszObjId** con el algoritmo hash deseado y los demás miembros según corresponda.
9.  Inicialice el [**\_ mensaje de signo de \_ \_ cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) para la estructura, inicializando el miembro **pSigningCert** con la dirección del certificado del firmante, el miembro de la matriz **MsgCert** en la dirección de los certificados del firmante y otros, el miembro **HashAlgorithm** en la dirección de la estructura del [**identificador del \_ algoritmo \_ de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier) y los demás miembros según corresponda.
10. Llame a la función [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) , pasando [**el \_ \_ mensaje de \_ signo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_sign_message_para) para el parámetro *pSignPara* , la dirección de la matriz de "datos que se van a firmar" para el parámetro *rgpbToBeSigned* , una dirección para el parámetro de salida *pbSignedBlob* y los valores para los demás parámetros, según corresponda.

 

 

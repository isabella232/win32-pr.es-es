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
# <a name="decrypting-data"></a><span data-ttu-id="9ad10-103">Descifrar datos</span><span class="sxs-lookup"><span data-stu-id="9ad10-103">Decrypting Data</span></span>

<span data-ttu-id="9ad10-104">En esta sección se presentan los pasos para descifrar un mensaje cifrado.</span><span class="sxs-lookup"><span data-stu-id="9ad10-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="9ad10-105">**Para descifrar un mensaje cifrado**</span><span class="sxs-lookup"><span data-stu-id="9ad10-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="9ad10-106">Obtiene un puntero al mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="9ad10-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="9ad10-107">Abra un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ad10-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="9ad10-108">En el mensaje, recupere el identificador de destinatario (My ID).</span><span class="sxs-lookup"><span data-stu-id="9ad10-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="9ad10-109">Use el identificador de destinatario para recuperar el certificado.</span><span class="sxs-lookup"><span data-stu-id="9ad10-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="9ad10-110">Obtiene la clave privada del certificado.</span><span class="sxs-lookup"><span data-stu-id="9ad10-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="9ad10-111">Use la clave privada para descifrar la clave simétrica (sesión).</span><span class="sxs-lookup"><span data-stu-id="9ad10-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="9ad10-112">Recupere el algoritmo de cifrado del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9ad10-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="9ad10-113">Descifre los datos mediante la clave de sesión descifrada y el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="9ad10-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="9ad10-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) realiza todas las tareas para descifrar un mensaje. sin embargo, todavía es necesario inicializar las estructuras y otros datos.</span><span class="sxs-lookup"><span data-stu-id="9ad10-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="9ad10-115">**Para descifrar datos mediante CryptDecryptMessage**</span><span class="sxs-lookup"><span data-stu-id="9ad10-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="9ad10-116">Obtiene un puntero al BLOB cifrado.</span><span class="sxs-lookup"><span data-stu-id="9ad10-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="9ad10-117">Abra un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ad10-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="9ad10-118">Cree una matriz de almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ad10-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="9ad10-119">Inicialice el [**\_ mensaje del descifrado del cifrado \_ \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) la estructura.</span><span class="sxs-lookup"><span data-stu-id="9ad10-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="9ad10-120">Llame a [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para descifrar los datos contenidos en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9ad10-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="9ad10-121">[Programa C de ejemplo: el uso de CryptEncryptMessage y CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa el procedimiento que se acaba de presentar.</span><span class="sxs-lookup"><span data-stu-id="9ad10-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="9ad10-122">Los comentarios muestran los elementos de código que realizan cada paso del procedimiento.</span><span class="sxs-lookup"><span data-stu-id="9ad10-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="9ad10-123">Para obtener más información sobre la función, vea [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)y para obtener más información sobre la estructura de datos, vea Crypt [**\_ descrypt \_ Message \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span><span class="sxs-lookup"><span data-stu-id="9ad10-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 




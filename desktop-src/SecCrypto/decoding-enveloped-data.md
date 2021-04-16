---
description: Tareas generales necesarias para descodificar un mensaje con doble cifrado.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Descodificar datos con doble cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550422"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="9da39-103">Descodificar datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="9da39-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="9da39-104">Las tareas generales necesarias para descodificar un mensaje con doble cifrado se muestran en la siguiente ilustración y se describen en la lista que lo sigue.</span><span class="sxs-lookup"><span data-stu-id="9da39-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![descodificar datos con doble cifrado](images/decemsg.png)

<span data-ttu-id="9da39-106">La secuencia de eventos para descodificar los datos con sobres mediante la administración de claves de transporte de claves, como se describe en la ilustración anterior, es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="9da39-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="9da39-107">Se recupera un puntero al mensaje con [*doble cifrado*](../secgloss/d-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9da39-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="9da39-108">Se abre un [*almacén de certificados*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9da39-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="9da39-109">En el mensaje, se recupera el identificador del destinatario (My ID).</span><span class="sxs-lookup"><span data-stu-id="9da39-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="9da39-110">El identificador de destinatario se usa para recuperar el certificado.</span><span class="sxs-lookup"><span data-stu-id="9da39-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="9da39-111">Se recupera la [*clave privada*](../secgloss/p-gly.md) asociada a ese certificado.</span><span class="sxs-lookup"><span data-stu-id="9da39-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="9da39-112">La clave privada se usa para descifrar la clave [*simétrica*](../secgloss/s-gly.md) ([*sesión*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="9da39-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="9da39-113">El algoritmo de cifrado se recupera del mensaje.</span><span class="sxs-lookup"><span data-stu-id="9da39-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="9da39-114">Con la clave privada y el algoritmo de cifrado, se descifran los datos.</span><span class="sxs-lookup"><span data-stu-id="9da39-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="9da39-115">En el procedimiento siguiente se usan funciones de mensaje de bajo nivel para realizar las tareas que se acaban de mostrar.</span><span class="sxs-lookup"><span data-stu-id="9da39-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="9da39-116">**Para descodificar un mensaje con doble cifrado**</span><span class="sxs-lookup"><span data-stu-id="9da39-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="9da39-117">Obtiene un puntero al objeto binario codificado.</span><span class="sxs-lookup"><span data-stu-id="9da39-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="9da39-118">Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.</span><span class="sxs-lookup"><span data-stu-id="9da39-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="9da39-119">Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso 2 y un puntero a los datos que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="9da39-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="9da39-120">Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="9da39-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="9da39-121">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando el identificador recuperado en el paso 2 y el \_ \_ parámetro de tipo CMSG para comprobar que el mensaje es del tipo de datos con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="9da39-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="9da39-122">Vuelva a llamar a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando \_ CMSG \_ parámetro de tipo de contenido interno \_ \_ para obtener el tipo de datos del [*contenido interno*](../secgloss/i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9da39-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="9da39-123">Si el tipo de datos de contenido interno son **datos**, continúe para descifrar y descodificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="9da39-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="9da39-124">De lo contrario, ejecute un procedimiento de descodificación apropiado para el tipo de datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="9da39-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="9da39-125">Suponiendo que el tipo de contenido interno sea "Data", inicialice [**CMSG \_ Ctrl \_ descrypt \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) la estructura de datos y llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), pasando el \_ \_ descifrado de CMSG Ctrl y la dirección de la estructura.</span><span class="sxs-lookup"><span data-stu-id="9da39-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="9da39-126">El contenido se descifrará.</span><span class="sxs-lookup"><span data-stu-id="9da39-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="9da39-127">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), pasando \_ el parámetro de contenido CMSG \_ para obtener un puntero al objeto binario de datos de contenido descodificado (cadena de **bytes** ).</span><span class="sxs-lookup"><span data-stu-id="9da39-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="9da39-128">Llame a [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) para cerrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="9da39-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="9da39-129">El resultado de este procedimiento es que el mensaje se descodifica y se descifra y se recupera un puntero al BLOB de datos de contenido.</span><span class="sxs-lookup"><span data-stu-id="9da39-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9da39-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9da39-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da39-131">Programa C de ejemplo: codificar un mensaje con signo de cifrado</span><span class="sxs-lookup"><span data-stu-id="9da39-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 

---
description: El motor del protocolo Schannel realiza el enlace y la autenticación en un proceso seguro y el cifrado o mensaje de forma masiva en el proceso de la aplicación.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Cruzar los límites del proceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686690"
---
# <a name="crossing-process-boundaries"></a><span data-ttu-id="8d7dd-103">Cruzar los límites del proceso</span><span class="sxs-lookup"><span data-stu-id="8d7dd-103">Crossing Process Boundaries</span></span>

<span data-ttu-id="8d7dd-104">El motor del protocolo [*Schannel*](../secgloss/s-gly.md) realiza el enlace y la autenticación en un [*proceso*](../secgloss/p-gly.md) seguro y el cifrado o mensaje de forma masiva en el proceso de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8d7dd-104">The [*Schannel*](../secgloss/s-gly.md) protocol engine performs the handshaking and authentication in a secure [*process*](../secgloss/p-gly.md) and the bulk encryption/message passing in the application process.</span></span> <span data-ttu-id="8d7dd-105">Esto significa que las [*claves de cifrado masivo*](../secgloss/b-gly.md) y las claves [*Mac*](../secgloss/m-gly.md) se deben copiar de un proceso a otro.</span><span class="sxs-lookup"><span data-stu-id="8d7dd-105">This means that the [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC*](../secgloss/m-gly.md) keys must be copied from one process to another.</span></span> <span data-ttu-id="8d7dd-106">Para copiar las claves de un proceso a otro, utilice las funciones [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) y [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8d7dd-106">To copy the keys from one process to another, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) functions as follows:</span></span>

1.  <span data-ttu-id="8d7dd-107">El proceso seguro exporta cada clave a un [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)y, a continuación, destruye la clave mediante [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="8d7dd-107">The secure process exports each key into an [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), then destroys the key using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span> <span data-ttu-id="8d7dd-108">Tenga en cuenta que si la clave se almacena en hardware, el CSP debe reconocerlo y no debe intentar destruir la clave.</span><span class="sxs-lookup"><span data-stu-id="8d7dd-108">Note that if the key is stored in hardware, the CSP must recognize this and must not attempt to destroy the key.</span></span>
2.  <span data-ttu-id="8d7dd-109">El proceso seguro pasa el OPAQUEKEYBLOBs al proceso de la aplicación de una forma más allá del ámbito de este documento.</span><span class="sxs-lookup"><span data-stu-id="8d7dd-109">The secure process passes the OPAQUEKEYBLOBs to the application process in a manner beyond the scope of this document.</span></span>
3.  <span data-ttu-id="8d7dd-110">El proceso de aplicación importa cada OPAQUEKEYBLOB de vuelta al CSP mediante [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="8d7dd-110">The application process imports each OPAQUEKEYBLOB back into the CSP using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="8d7dd-111">En este punto, la clave debe estar exactamente en el mismo [*Estado*](../secgloss/s-gly.md) en que se exportó.</span><span class="sxs-lookup"><span data-stu-id="8d7dd-111">At this point, the key must be in exactly the same [*state*](../secgloss/s-gly.md) as when it was exported.</span></span>

 

 

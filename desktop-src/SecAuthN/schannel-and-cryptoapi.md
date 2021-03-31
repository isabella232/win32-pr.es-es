---
description: Schannel usa CryptoAPI para operaciones criptográficas, como el almacenamiento de claves públicas y privadas.
ms.assetid: 5ad9a171-5f69-4035-aac5-ae8d27d0abfb
title: Schannel y CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0684cd690911444b77ba27d2876e578fd71c73a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423624"
---
# <a name="schannel-and-cryptoapi"></a><span data-ttu-id="db874-103">Schannel y CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="db874-103">Schannel and CryptoAPI</span></span>

<span data-ttu-id="db874-104">Schannel usa [CryptoAPI](../seccrypto/cryptography-essentials.md) para operaciones criptográficas, como el almacenamiento de [*claves públicas y privadas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="db874-104">Schannel uses [CryptoAPI](../seccrypto/cryptography-essentials.md) for cryptographic operations such as storing [*public/private keys*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="db874-105">En los temas siguientes se proporciona información detallada acerca de cómo Schannel usa CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="db874-105">The following topics provide detailed information about how Schannel makes use of CryptoAPI.</span></span>



| <span data-ttu-id="db874-106">Tema</span><span class="sxs-lookup"><span data-stu-id="db874-106">Topic</span></span>                                                                   | <span data-ttu-id="db874-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="db874-107">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db874-108">Almacenes de certificados</span><span class="sxs-lookup"><span data-stu-id="db874-108">Certificate Stores</span></span>](certificate-stores.md)<br/>                 | <span data-ttu-id="db874-109">Los certificados de cliente y de servidor deben almacenarse en un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="db874-109">Both client and server certificates must be stored in a certificate store.</span></span><br/>                                |
| [<span data-ttu-id="db874-110">CryptoAPI 2.0 claves privadas</span><span class="sxs-lookup"><span data-stu-id="db874-110">CryptoAPI 2.0 Private Keys</span></span>](cryptoapi-2-0-private-keys.md)<br/> | <span data-ttu-id="db874-111">Las credenciales de Schannel se representan internamente como estructuras de [**\_ contexto de certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="db874-111">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span><br/> |



 

 

 

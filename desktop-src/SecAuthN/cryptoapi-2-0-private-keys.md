---
description: Las credenciales de Schannel se representan internamente como estructuras de contexto de certificado \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 claves privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648463"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="2a669-103">CryptoAPI 2.0 claves privadas</span><span class="sxs-lookup"><span data-stu-id="2a669-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="2a669-104">Las credenciales de Schannel se representan internamente como estructuras de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="2a669-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="2a669-105">Schannel busca la [*clave privada*](/windows/desktop/SecGloss/p-gly) asociada a un contexto de certificado determinado mediante la propiedad de certificado de la clave de la información de identificador de la clave de certificado del certificado \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a669-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="2a669-106">Con esta propiedad, Schannel obtiene acceso a la *clave privada* mediante una llamada a la función [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="2a669-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="2a669-107">Para obtener más información, vea [pares de claves pública y privada](/windows/desktop/SecCrypto/public-private-key-pairs).</span><span class="sxs-lookup"><span data-stu-id="2a669-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="2a669-108">Cada credencial Schannel contiene una referencia a una o varias claves privadas, cada una asociada a un certificado determinado.</span><span class="sxs-lookup"><span data-stu-id="2a669-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="2a669-109">Las [*claves privadas*](/windows/desktop/SecGloss/p-gly) se tratan de forma bastante diferente en función de si la credencial es para un cliente o un servidor.</span><span class="sxs-lookup"><span data-stu-id="2a669-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="2a669-110">Claves privadas de cliente</span><span class="sxs-lookup"><span data-stu-id="2a669-110">Client Private Keys</span></span>

<span data-ttu-id="2a669-111">El [*proveedor de servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) administra las [*claves privadas*](/windows/desktop/SecGloss/p-gly) del cliente en uso.</span><span class="sxs-lookup"><span data-stu-id="2a669-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="2a669-112">Normalmente, las claves privadas de cliente las almacenan los CSP de la firma RSA [ \_ \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) o Prov \_ RSA \_ .</span><span class="sxs-lookup"><span data-stu-id="2a669-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="2a669-113">Si la aplicación cliente hace que la llamada a [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) sea manual, antes de llamar a [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), el cliente debe enlazar el identificador del CSP con el contexto de certificado mediante la propiedad de identificador de prop identificador de la clave de certificado \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a669-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="2a669-114">Si Schannel encuentra este conjunto de propiedades, no utiliza la propiedad del identificador de propiedades de la clave de certificado \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2a669-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="2a669-115">Claves privadas de servidor</span><span class="sxs-lookup"><span data-stu-id="2a669-115">Server Private Keys</span></span>

<span data-ttu-id="2a669-116">Las claves privadas del servidor se almacenan en uno de los siguientes CSP:</span><span class="sxs-lookup"><span data-stu-id="2a669-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="2a669-117">aprovisionamiento de \_ RSA \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="2a669-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="2a669-118">PROV \_ DH \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="2a669-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="2a669-119">CSP de PROV \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="2a669-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="2a669-120">La elección de CSP depende del algoritmo de [*intercambio de claves*](/windows/desktop/SecGloss/k-gly)seleccionado.</span><span class="sxs-lookup"><span data-stu-id="2a669-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="2a669-121">Las claves privadas del servidor deben ser de tipo en \_ KEYEXCHANGE.</span><span class="sxs-lookup"><span data-stu-id="2a669-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 

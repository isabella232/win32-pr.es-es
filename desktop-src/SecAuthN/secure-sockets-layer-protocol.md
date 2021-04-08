---
description: La información de este tema se aplica a Windows Server 2003 y Windows XP.
ms.assetid: 45536902-af80-4dca-b3ce-207086844763
title: Protocolo Capa de sockets seguros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ed2555c854a6cc25948abe0dc83043ee632170
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001848"
---
# <a name="secure-sockets-layer-protocol"></a><span data-ttu-id="f1107-103">Protocolo Capa de sockets seguros</span><span class="sxs-lookup"><span data-stu-id="f1107-103">Secure Sockets Layer Protocol</span></span>

<span data-ttu-id="f1107-104">La información de este tema se aplica a Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1107-104">The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f1107-105">Para los conjuntos de cifrado para Windows Server 2008 y Windows Vista, consulte [conjuntos de cifrado en Schannel](cipher-suites-in-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="f1107-105">For cipher suites for Windows Server 2008 and Windows Vista, see [Cipher Suites in Schannel](cipher-suites-in-schannel.md).</span></span>

<span data-ttu-id="f1107-106">Schannel admite las versiones 2,0 y 3,0 del [*protocolo capa de sockets seguros (SSL)*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f1107-106">Schannel supports versions 2.0 and 3.0 of the [*Secure Sockets Layer (SSL) protocol*](../secgloss/s-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="f1107-107">A partir de Windows 10, versión 1607 y Windows Server 2016, se ha quitado SSL 2,0 y ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="f1107-107">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

 

## <a name="ssl-30"></a><span data-ttu-id="f1107-108">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="f1107-108">SSL 3.0</span></span>

<span data-ttu-id="f1107-109">SSL 3,0 es el predecesor del Protocolo de seguridad de la [capa de transporte](transport-layer-security-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="f1107-109">SSL 3.0 is the predecessor of the [Transport Layer Security Protocol](transport-layer-security-protocol.md).</span></span>

<span data-ttu-id="f1107-110">Schannel admite los conjuntos de cifrado que aparecen en [conjuntos de cifrado TLS](tls-cipher-suites.md) para SSL 3,0.</span><span class="sxs-lookup"><span data-stu-id="f1107-110">Schannel supports the cipher suites listed under [TLS Cipher Suites](tls-cipher-suites.md) for SSL 3.0.</span></span> <span data-ttu-id="f1107-111">SSL 3,0 es compatible con todos los conjuntos de cifrado que se enumeran en conjuntos de cifrado TLS y SSL \_ Fortezza \_ Kea \_ con \_ Fortezza \_ CBC \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="f1107-111">SSL 3.0 supports all of the cipher suites listed under TLS Cipher Suites as well as SSL\_FORTEZZA\_KEA\_WITH\_FORTEZZA\_CBC\_SHA.</span></span>

## <a name="ssl-20"></a><span data-ttu-id="f1107-112">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="f1107-112">SSL 2.0</span></span>

<span data-ttu-id="f1107-113">SSL 2,0 se ha sustituido por TLS y no debe usarse para el nuevo desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f1107-113">SSL 2.0 has been superseded by TLS and should not be used for new development.</span></span>

<span data-ttu-id="f1107-114">Schannel admite los siguientes conjuntos de cifrado para SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="f1107-114">Schannel supports the following cipher suites for SSL 2.0.</span></span> <span data-ttu-id="f1107-115">Los conjuntos se muestran en orden de más seguro a menos seguro.</span><span class="sxs-lookup"><span data-stu-id="f1107-115">The suites are listed in order from most secure to least secure.</span></span>

-   <span data-ttu-id="f1107-116">SSL \_ RC4 \_ 128 \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="f1107-116">SSL\_RC4\_128\_WITH\_MD5</span></span>
-   <span data-ttu-id="f1107-117">SSL \_ DES \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="f1107-117">SSL\_DES\_192\_EDE3\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="f1107-118">SSL \_ RC2 \_ CBC \_ \_ de 128 CBC \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="f1107-118">SSL\_RC2\_CBC\_128\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="f1107-119">SSL \_ DES \_ 64 \_ CBC \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="f1107-119">SSL\_DES\_64\_CBC\_WITH\_MD5</span></span>
-   <span data-ttu-id="f1107-120">SSL \_ RC4 \_ 128 \_ EXPORT40 \_ con \_ MD5</span><span class="sxs-lookup"><span data-stu-id="f1107-120">SSL\_RC4\_128\_EXPORT40\_WITH\_MD5</span></span>

 

 

---
description: Crypt32.dll es el módulo que implementa muchas de las funciones de CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Crypt32.dll versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809343"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="8c696-103">Crypt32.dll versiones</span><span class="sxs-lookup"><span data-stu-id="8c696-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="8c696-104">Crypt32.dll es el módulo que implementa muchas de las funciones de mensajería criptográfica y de certificado en la CryptoAPI, como [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="8c696-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="8c696-105">Crypt32.dll es un módulo que se incluye con los sistemas operativos Windows y Windows Server, pero las distintas versiones de este archivo DLL proporcionan diferentes capacidades.</span><span class="sxs-lookup"><span data-stu-id="8c696-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="8c696-106">No hay ninguna API para determinar la versión de CryptoAPI que está en uso, pero puede determinar la versión de Crypt32.dll que se está usando actualmente con las funciones [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) y [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .</span><span class="sxs-lookup"><span data-stu-id="8c696-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="8c696-107">En general, los intervalos de versión de Crypt32.dll se asignan a las versiones del sistema operativo, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c696-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="8c696-108">Sin embargo, esta tabla se debe utilizar como directriz solo porque es posible, a través de otras vías de actualización, que la versión Crypt32.dll diferirá de la indicada en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8c696-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="8c696-109">Versión de Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="8c696-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="8c696-110">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8c696-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c696-111">*versión* >= 5.131.3790.0</span><span class="sxs-lookup"><span data-stu-id="8c696-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="8c696-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c696-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="8c696-113">*versión* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="8c696-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="8c696-114">Windows XP con Service Pack 2 (SP2) Windows XP con Service Pack 1 (SP1) con la revisión [Q329433](https://support.microsoft.com/kb/329433)</span><span class="sxs-lookup"><span data-stu-id="8c696-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="8c696-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c696-115">Windows XP</span></span><br/> |
| <span data-ttu-id="8c696-116">5.131.2600.0 <= *versión* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="8c696-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="8c696-117">Windows XP con SP1Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c696-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 

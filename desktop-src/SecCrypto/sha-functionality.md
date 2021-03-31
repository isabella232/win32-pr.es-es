---
description: El proveedor base original comunicó incorrectamente que el algoritmo hash SHA enumera los algoritmos mediante llamadas a CryptGetProvParam con el parámetro PP \_ ENUMALGS especificado.
ms.assetid: 75128a4f-273a-4195-b206-30fc8bc589e9
title: Funcionalidad SHA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8a06ce5c11dfaa00e2ec7ee3427dfda2f8b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808318"
---
# <a name="sha-functionality"></a><span data-ttu-id="61371-103">Funcionalidad SHA</span><span class="sxs-lookup"><span data-stu-id="61371-103">SHA Functionality</span></span>

<span data-ttu-id="61371-104">El proveedor base original comunicó incorrectamente que el algoritmo hash [*Sha*](../secgloss/s-gly.md) enumera los algoritmos mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el parámetro PP \_ ENUMALGS especificado.</span><span class="sxs-lookup"><span data-stu-id="61371-104">The original Base Provider incorrectly reported that the [*SHA*](../secgloss/s-gly.md) hash algorithm enumerating algorithms by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with parameter PP\_ENUMALGS specified.</span></span> <span data-ttu-id="61371-105">Esto se ha corregido en el proveedor base.</span><span class="sxs-lookup"><span data-stu-id="61371-105">This has been fixed in the Base Provider.</span></span> <span data-ttu-id="61371-106">Tanto el proveedor base revisado como el proveedor extendido y ahora notifican correctamente a SHA-1.</span><span class="sxs-lookup"><span data-stu-id="61371-106">Both the revised Base Provider and the Extended Provider and now correctly report SHA-1.</span></span>

<span data-ttu-id="61371-107">Se ha \_ agregado una constante CALG SHA1 definida a Wincrypt. h con el mismo valor que CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="61371-107">A defined CALG\_SHA1 constant has been added to Wincrypt.h with the same value as CALG\_SHA.</span></span>

 

 

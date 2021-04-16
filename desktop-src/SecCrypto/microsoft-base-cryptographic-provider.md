---
description: El proveedor de servicios criptográficos básicos de Microsoft es el proveedor de proveedores de servicios criptográficos (CSP) inicial y se distribuye con las versiones de CryptoAPI 1,0 y 2,0. Es un proveedor de uso general que admite firmas digitales y cifrado de datos.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Proveedor de servicios criptográficos básicos de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686866"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="5756c-104">Proveedor de servicios criptográficos básicos de Microsoft</span><span class="sxs-lookup"><span data-stu-id="5756c-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="5756c-105">El proveedor de servicios criptográficos básicos de Microsoft es el proveedor de [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) (CSP) inicial y se distribuye con las versiones de [*CryptoAPI*](../secgloss/c-gly.md) 1,0 y 2,0.</span><span class="sxs-lookup"><span data-stu-id="5756c-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="5756c-106">Es un proveedor de uso general que admite [*firmas digitales*](../secgloss/d-gly.md) y cifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="5756c-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="5756c-107">El algoritmo de clave pública RSA se utiliza para todas las operaciones de clave pública.</span><span class="sxs-lookup"><span data-stu-id="5756c-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="5756c-108">Para mantener la compatibilidad con versiones anteriores con versiones anteriores, la nueva versión del proveedor conserva la designación de la versión 1,0 del nombre en Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="5756c-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="5756c-109">Sin embargo, la versión 2,0 de este proveedor se está distribuyendo actualmente.</span><span class="sxs-lookup"><span data-stu-id="5756c-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="5756c-110">Para determinar la versión real del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **la \_ versión PP**.</span><span class="sxs-lookup"><span data-stu-id="5756c-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="5756c-111">Si 0x0200 se devuelve en *pbData*, tendrá la versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="5756c-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                |                     |
|----------------|---------------------|
| <span data-ttu-id="5756c-112">Tipo de proveedor:</span><span class="sxs-lookup"><span data-stu-id="5756c-112">Provider type:</span></span> | <span data-ttu-id="5756c-113">**aprovisionamiento \_ completo de RSA \_**</span><span class="sxs-lookup"><span data-stu-id="5756c-113">**PROV\_RSA\_FULL**</span></span> |
| <span data-ttu-id="5756c-114">Nombre del proveedor:</span><span class="sxs-lookup"><span data-stu-id="5756c-114">Provider name:</span></span> | <span data-ttu-id="5756c-115">**Prov de MS \_ Def \_**</span><span class="sxs-lookup"><span data-stu-id="5756c-115">**MS\_DEF\_PROV**</span></span>   |



 

 

 

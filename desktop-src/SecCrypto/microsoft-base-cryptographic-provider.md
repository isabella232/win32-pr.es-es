---
description: El proveedor criptográfico base de Microsoft es el proveedor de servicios criptográficos inicial (CSP) y se distribuye con las versiones 1.0 y 2.0 de CryptoAPI. Es un proveedor de uso general que admite firmas digitales y cifrado de datos.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Proveedor criptográfico base de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581893"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="56b6b-104">Proveedor criptográfico base de Microsoft</span><span class="sxs-lookup"><span data-stu-id="56b6b-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="56b6b-105">El proveedor criptográfico base de Microsoft es el proveedor de [*servicios*](../secgloss/c-gly.md) criptográficos inicial (CSP) y se distribuye con las versiones 1.0 y 2.0 de [*CryptoAPI.*](../secgloss/c-gly.md)</span><span class="sxs-lookup"><span data-stu-id="56b6b-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="56b6b-106">Es un proveedor de uso general que admite firmas [*digitales y*](../secgloss/d-gly.md) cifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="56b6b-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="56b6b-107">El algoritmo de clave pública RSA se usa para todas las operaciones de clave pública.</span><span class="sxs-lookup"><span data-stu-id="56b6b-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="56b6b-108">Para mantener la compatibilidad con versiones anteriores, la nueva versión del proveedor conserva la designación de la versión 1.0 del nombre en Wincrypt.h.</span><span class="sxs-lookup"><span data-stu-id="56b6b-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="56b6b-109">Sin embargo, la versión 2.0 de este proveedor se está enviando actualmente.</span><span class="sxs-lookup"><span data-stu-id="56b6b-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="56b6b-110">Para determinar la versión real del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **PP \_ VERSION**.</span><span class="sxs-lookup"><span data-stu-id="56b6b-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="56b6b-111">Si 0x0200 se devuelve en *pbData*, tiene la versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="56b6b-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                   | <span data-ttu-id="56b6b-112">Value</span><span class="sxs-lookup"><span data-stu-id="56b6b-112">Value</span></span>            |
|-------------------|------------------|
| <span data-ttu-id="56b6b-113">**Tipo de proveedor**</span><span class="sxs-lookup"><span data-stu-id="56b6b-113">**Provider type**</span></span> | <span data-ttu-id="56b6b-114">PROV \_ RSA \_ FULL</span><span class="sxs-lookup"><span data-stu-id="56b6b-114">PROV\_RSA\_FULL</span></span>  |
| <span data-ttu-id="56b6b-115">**Nombre del proveedor**</span><span class="sxs-lookup"><span data-stu-id="56b6b-115">**Provider name**</span></span> | <span data-ttu-id="56b6b-116">MS \_ DEF \_ PROV</span><span class="sxs-lookup"><span data-stu-id="56b6b-116">MS\_DEF\_PROV</span></span>    |



 

 

 

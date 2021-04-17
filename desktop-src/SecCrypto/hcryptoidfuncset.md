---
description: Representa un identificador para un conjunto de funciones instalables de identificador de objetos (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668212"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="a64f0-103">HCRYPTOIDFUNCSET</span><span class="sxs-lookup"><span data-stu-id="a64f0-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="a64f0-104">El tipo de datos **HCRYPTOIDFUNCSET** representa un identificador para un conjunto de funciones instalables de [*identificador de objetos*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="a64f0-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="a64f0-105">Las funciones [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)y [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) utilizan este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="a64f0-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="a64f0-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a64f0-106">Requirements</span></span>



| <span data-ttu-id="a64f0-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="a64f0-107">Requirement</span></span> | <span data-ttu-id="a64f0-108">Value</span><span class="sxs-lookup"><span data-stu-id="a64f0-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a64f0-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a64f0-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a64f0-110">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a64f0-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a64f0-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a64f0-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a64f0-112">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="a64f0-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a64f0-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a64f0-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="a64f0-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64f0-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 

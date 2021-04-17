---
description: Representa un identificador de una función instalable de identificador de objetos (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668211"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="d6c7e-103">HCRYPTOIDFUNCADDR</span><span class="sxs-lookup"><span data-stu-id="d6c7e-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="d6c7e-104">El tipo de datos **HCRYPTOIDFUNCADDR** representa un identificador de una función instalable de [*identificador de objetos*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="d6c7e-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="d6c7e-105">Las funciones [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)y [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , y la estructura [**de \_ \_ \_ información del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) usan este tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="d6c7e-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="d6c7e-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c7e-106">Requirements</span></span>



| <span data-ttu-id="d6c7e-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c7e-107">Requirement</span></span> | <span data-ttu-id="d6c7e-108">Value</span><span class="sxs-lookup"><span data-stu-id="d6c7e-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c7e-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6c7e-109">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c7e-110">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d6c7e-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6c7e-111">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c7e-112">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c7e-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d6c7e-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6c7e-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c7e-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c7e-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 

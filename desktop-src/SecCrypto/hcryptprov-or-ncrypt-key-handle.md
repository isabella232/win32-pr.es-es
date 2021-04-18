---
description: Se utiliza como identificador de un proveedor de servicios criptográficos (CSP) de CryptoAPI o CSP de CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668210"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="cb72b-103">\_identificador de clave HCRYPTPROV o \_ NCRYPT \_ \_</span><span class="sxs-lookup"><span data-stu-id="cb72b-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="cb72b-104">El tipo de datos de **\_ identificador de clave HCRYPTPROV o \_ NCRYPT \_ \_** se utiliza como identificador de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) de CryptoAPI o un CSP de CNG.</span><span class="sxs-lookup"><span data-stu-id="cb72b-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="cb72b-105">Este identificador debe ser un identificador de [**HCRYPTPROV**](hcryptprov.md) que se haya creado mediante la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) o un identificador de **\_ \_ identificador de clave NCRYPT** que se haya creado mediante la función [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="cb72b-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="cb72b-106">Las nuevas aplicaciones siempre deben pasar el identificador de **\_ \_ identificador de clave NCRYPT** a un CSP de CNG.</span><span class="sxs-lookup"><span data-stu-id="cb72b-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="cb72b-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb72b-107">Requirements</span></span>



| <span data-ttu-id="cb72b-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb72b-108">Requirement</span></span> | <span data-ttu-id="cb72b-109">Value</span><span class="sxs-lookup"><span data-stu-id="cb72b-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb72b-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb72b-110">Minimum supported client</span></span><br/> | <span data-ttu-id="cb72b-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb72b-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb72b-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb72b-112">Minimum supported server</span></span><br/> | <span data-ttu-id="cb72b-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb72b-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb72b-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb72b-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb72b-115"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb72b-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 

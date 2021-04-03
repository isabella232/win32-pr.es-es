---
description: Identificador del objeto de directiva local.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082705"
---
# <a name="lsa_handle"></a><span data-ttu-id="6c2b8-103">identificador de LSA \_</span><span class="sxs-lookup"><span data-stu-id="6c2b8-103">LSA\_HANDLE</span></span>

<span data-ttu-id="6c2b8-104">El tipo de datos de **\_ identificador de LSA** es un identificador del objeto de [**Directiva**](policy-object.md) local.</span><span class="sxs-lookup"><span data-stu-id="6c2b8-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="6c2b8-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c2b8-105">Remarks</span></span>

<span data-ttu-id="6c2b8-106">Antes de poder usar la API de directiva local, la aplicación debe abrir un identificador de un objeto de [**Directiva**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6c2b8-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="6c2b8-107">Para ello, llame a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span><span class="sxs-lookup"><span data-stu-id="6c2b8-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="6c2b8-108">Esta función devuelve un identificador que la aplicación puede especificar en las siguientes llamadas de función de directiva de LSA.</span><span class="sxs-lookup"><span data-stu-id="6c2b8-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="6c2b8-109">Cada controlador tiene un conjunto asociado de permisos que determinan las operaciones que puede realizar la aplicación en el objeto de [**Directiva**](policy-object.md) mediante el uso del identificador.</span><span class="sxs-lookup"><span data-stu-id="6c2b8-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="6c2b8-110">La aplicación puede abrir más de un identificador para el objeto de **Directiva** a la vez.</span><span class="sxs-lookup"><span data-stu-id="6c2b8-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="6c2b8-111">Cuando ya no se necesita un identificador, la aplicación debe cerrarlo llamando a [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span><span class="sxs-lookup"><span data-stu-id="6c2b8-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2b8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c2b8-112">Requirements</span></span>



| <span data-ttu-id="6c2b8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c2b8-113">Requirement</span></span> | <span data-ttu-id="6c2b8-114">Value</span><span class="sxs-lookup"><span data-stu-id="6c2b8-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2b8-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c2b8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2b8-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6c2b8-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6c2b8-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c2b8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2b8-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c2b8-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c2b8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c2b8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c2b8-120"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c2b8-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2b8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c2b8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2b8-122">**LsaClose**</span><span class="sxs-lookup"><span data-stu-id="6c2b8-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="6c2b8-123">**LsaOpenPolicy**</span><span class="sxs-lookup"><span data-stu-id="6c2b8-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 


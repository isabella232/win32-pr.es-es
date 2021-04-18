---
description: 'El tipo de datos de identificador de la \_ enumeración LSA \_ lo usa la función LSA que enumera los objetos TrustedDomain: LsaEnumerateTrustedDomainsEx.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687574"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="21596-103">\_identificador de enumeración de LSA \_</span><span class="sxs-lookup"><span data-stu-id="21596-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="21596-104">El tipo de datos de identificador de la **\_ enumeración \_ LSA** lo usa la función LSA que enumera los objetos [**TrustedDomain**](trusteddomain-object.md) : [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="21596-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="21596-105">Esta función está diseñada para que pueda realizar varias llamadas para enumerar todos los objetos de un tipo determinado en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="21596-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="21596-106">En la llamada de función de enumeración inicial, se pasa un puntero a una variable de **\_ \_ identificador de enumeración de LSA** que se inicializa en cero.</span><span class="sxs-lookup"><span data-stu-id="21596-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="21596-107">La función actualiza este valor.</span><span class="sxs-lookup"><span data-stu-id="21596-107">The function updates this value.</span></span> <span data-ttu-id="21596-108">Si la función devuelve un valor que indica que hay más objetos para enumerar, llame de nuevo a la función y pase el valor de identificador de la **\_ \_ enumeración LSA** actualizado para obtener una enumeración que continúe desde el punto en el que se quedó la enumeración anterior.</span><span class="sxs-lookup"><span data-stu-id="21596-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="21596-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21596-109">Requirements</span></span>



| <span data-ttu-id="21596-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="21596-110">Requirement</span></span> | <span data-ttu-id="21596-111">Value</span><span class="sxs-lookup"><span data-stu-id="21596-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21596-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21596-112">Minimum supported client</span></span><br/> | <span data-ttu-id="21596-113">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="21596-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="21596-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21596-114">Minimum supported server</span></span><br/> | <span data-ttu-id="21596-115">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="21596-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21596-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21596-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="21596-117"><dt>Ntsecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="21596-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21596-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="21596-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21596-119">**LsaEnumerateTrustedDomainsEx**</span><span class="sxs-lookup"><span data-stu-id="21596-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 





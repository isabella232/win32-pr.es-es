---
title: Tipos de datos del servicio de acceso remoto (RAS. h)
description: La API del servicio de acceso remoto usa los siguientes tipos de datos.
ms.assetid: aaa7f971-9c23-4738-a386-9b7db859f6be
keywords:
- RASIPV4ADDR
- RASIPV6ADDR
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8aa2fdae531c5aae0986d3289802565c6914fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996358"
---
# <a name="remote-access-service-data-types"></a><span data-ttu-id="fd60c-105">Tipos de datos del servicio de acceso remoto</span><span class="sxs-lookup"><span data-stu-id="fd60c-105">Remote Access Service Data Types</span></span>

<span data-ttu-id="fd60c-106">La API del servicio de acceso remoto usa los siguientes tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="fd60c-106">The following data types are used by the Remote Access Service API.</span></span>


```C++
typedef in_addr RASIPV4ADDR;
typedef in6_addr RASIPV6ADDR;
```



<dl> <dt>

<span data-ttu-id="fd60c-107">**RASIPV4ADDR**</span><span class="sxs-lookup"><span data-stu-id="fd60c-107">**RASIPV4ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="fd60c-108">[**En \_ addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) que contiene una dirección IPv4.</span><span class="sxs-lookup"><span data-stu-id="fd60c-108">A [**in\_addr**](/windows/desktop/api/winsock2/ns-winsock2-in_addr) that contains an IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="fd60c-109">Compatible con Windows Vista o versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fd60c-109">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> <dt>

<span data-ttu-id="fd60c-110">**RASIPV6ADDR**</span><span class="sxs-lookup"><span data-stu-id="fd60c-110">**RASIPV6ADDR**</span></span>
</dt> <dd>

<span data-ttu-id="fd60c-111">Una [**dirección \_ IN6**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) que contiene una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="fd60c-111">A [**in6\_addr**](/previous-versions/windows/desktop/legacy/ms738560(v=vs.85)) that contains an IPv6 address.</span></span>

> [!Note]  
> <span data-ttu-id="fd60c-112">Compatible con Windows Vista o versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="fd60c-112">Supported in Windows Vista or later versions of Windows.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd60c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd60c-113">Requirements</span></span>



| <span data-ttu-id="fd60c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd60c-114">Requirement</span></span> | <span data-ttu-id="fd60c-115">Value</span><span class="sxs-lookup"><span data-stu-id="fd60c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fd60c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd60c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd60c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd60c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fd60c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd60c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd60c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd60c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fd60c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd60c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd60c-121"><dt>Ras. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd60c-121"><dt>Ras.h</dt></span></span> </dl> |



 


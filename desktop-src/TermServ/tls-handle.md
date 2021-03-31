---
title: TLS_HANDLE
description: Representa un identificador de un servidor de licencias de Escritorio remoto.
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09764072b42e14aea2d1b8242dbc3cbb044442b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801687"
---
# <a name="tls_handle"></a><span data-ttu-id="0657a-104">identificador de TLS \_</span><span class="sxs-lookup"><span data-stu-id="0657a-104">TLS\_HANDLE</span></span>

<span data-ttu-id="0657a-105">Representa un identificador de un servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="0657a-105">Represents a handle to a Remote Desktop license server.</span></span> <span data-ttu-id="0657a-106">La función [**TLSConnectToLsServer**](tlsconnecttolsserver.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="0657a-106">This handle is returned by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="0657a-107">Este tipo de datos no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="0657a-107">This data type has no associated header file.</span></span> <span data-ttu-id="0657a-108">Para usarlo, debe definirlo como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="0657a-108">To use it, you must define it yourself as shown in this topic.</span></span>

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="0657a-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0657a-109">Requirements</span></span>



| <span data-ttu-id="0657a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0657a-110">Requirement</span></span> | <span data-ttu-id="0657a-111">Value</span><span class="sxs-lookup"><span data-stu-id="0657a-111">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0657a-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0657a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0657a-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0657a-113">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0657a-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0657a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0657a-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0657a-115">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0657a-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0657a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0657a-117">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="0657a-117">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="0657a-118">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="0657a-118">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

 






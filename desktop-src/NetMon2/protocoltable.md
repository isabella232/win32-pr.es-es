---
description: La estructura PROTOCOLTABLE contiene una lista de protocolos.
ms.assetid: dad2b228-5916-44fe-b78e-ebc6507dc555
title: Estructura PROTOCOLTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3ad79beca7ce79611747a02704ffc05da5fc3d4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678177"
---
# <a name="protocoltable-structure"></a><span data-ttu-id="c8f8c-103">Estructura PROTOCOLTABLE</span><span class="sxs-lookup"><span data-stu-id="c8f8c-103">PROTOCOLTABLE structure</span></span>

<span data-ttu-id="c8f8c-104">La estructura **PROTOCOLTABLE** contiene una lista de protocolos.</span><span class="sxs-lookup"><span data-stu-id="c8f8c-104">The **PROTOCOLTABLE** structure contains a list of protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f8c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8f8c-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLTABLE {
  DWORD     nProtocols;
  HPROTOCOL hProtocol[1];
} PROTOCOLTABLE;
```



## <a name="members"></a><span data-ttu-id="c8f8c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8f8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8f8c-107">**nProtocols**</span><span class="sxs-lookup"><span data-stu-id="c8f8c-107">**nProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c8f8c-108">Número de protocolos habilitados.</span><span class="sxs-lookup"><span data-stu-id="c8f8c-108">Number of protocols that are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="c8f8c-109">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="c8f8c-109">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="c8f8c-110">Matriz de identificadores para protocolos habilitados.</span><span class="sxs-lookup"><span data-stu-id="c8f8c-110">Array of handles to enabled protocols.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8f8c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8f8c-111">Requirements</span></span>



| <span data-ttu-id="c8f8c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f8c-112">Requirement</span></span> | <span data-ttu-id="c8f8c-113">Value</span><span class="sxs-lookup"><span data-stu-id="c8f8c-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f8c-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8f8c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f8c-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c8f8c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c8f8c-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8f8c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f8c-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8f8c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c8f8c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8f8c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f8c-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8f8c-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 





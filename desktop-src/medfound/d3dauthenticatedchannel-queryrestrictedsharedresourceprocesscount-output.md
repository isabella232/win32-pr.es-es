---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808137"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="1370a-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="1370a-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="1370a-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .</span><span class="sxs-lookup"><span data-stu-id="1370a-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="1370a-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="1370a-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="1370a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1370a-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="1370a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1370a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1370a-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="1370a-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="1370a-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="1370a-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="1370a-110">**NumRestrictedSharedResourceProcesses**</span><span class="sxs-lookup"><span data-stu-id="1370a-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="1370a-111">El número de procesos que pueden abrir recursos compartidos con acceso restringido.</span><span class="sxs-lookup"><span data-stu-id="1370a-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="1370a-112">Un proceso no puede abrir este tipo de recurso a menos que se haya concedido acceso al proceso.</span><span class="sxs-lookup"><span data-stu-id="1370a-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1370a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1370a-113">Requirements</span></span>



| <span data-ttu-id="1370a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1370a-114">Requirement</span></span> | <span data-ttu-id="1370a-115">Value</span><span class="sxs-lookup"><span data-stu-id="1370a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1370a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1370a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1370a-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1370a-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1370a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1370a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1370a-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1370a-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1370a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1370a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1370a-121"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1370a-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1370a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="1370a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1370a-123">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1370a-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="1370a-124">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="1370a-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 





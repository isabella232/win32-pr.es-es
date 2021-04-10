---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS.
ms.assetid: 763c56b5-b240-4bad-b601-07959ed37479
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: bd93e1cadb7da500a82218924044af79fbb1f493
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153650"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_output-structure"></a><span data-ttu-id="328c0-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_</span><span class="sxs-lookup"><span data-stu-id="328c0-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT structure</span></span>

<span data-ttu-id="328c0-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .</span><span class="sxs-lookup"><span data-stu-id="328c0-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="328c0-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="328c0-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="328c0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="328c0-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT          Output;
  UINT                                          ProcessIndex;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentifer;
  HANDLE                                        ProcessHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="328c0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="328c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="328c0-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="328c0-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="328c0-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="328c0-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="328c0-110">**ProcessIndex**</span><span class="sxs-lookup"><span data-stu-id="328c0-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="328c0-111">Índice del proceso en la lista de procesos.</span><span class="sxs-lookup"><span data-stu-id="328c0-111">The index of the process in the list of processes.</span></span>

</dd> <dt>

<span data-ttu-id="328c0-112">**ProcessIdentifer**</span><span class="sxs-lookup"><span data-stu-id="328c0-112">**ProcessIdentifer**</span></span>
</dt> <dd>

<span data-ttu-id="328c0-113">Un valor de [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) que especifica el tipo de proceso.</span><span class="sxs-lookup"><span data-stu-id="328c0-113">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span>

</dd> <dt>

<span data-ttu-id="328c0-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="328c0-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="328c0-115">Identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="328c0-115">A process handle.</span></span> <span data-ttu-id="328c0-116">Si el miembro **ProcessIdentifier** es igual que el **\_ identificador PROCESSIDTYPE**, el miembro **ProcessHandle** contiene un identificador válido para un proceso.</span><span class="sxs-lookup"><span data-stu-id="328c0-116">If the **ProcessIdentifier** member equals **PROCESSIDTYPE\_HANDLE**, the **ProcessHandle** member contains a valid handle to a process.</span></span> <span data-ttu-id="328c0-117">De lo contrario, se omite este miembro.</span><span class="sxs-lookup"><span data-stu-id="328c0-117">Otherwise, this member is ignored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="328c0-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="328c0-118">Remarks</span></span>

<span data-ttu-id="328c0-119">El proceso Administrador de ventanas de escritorio (DWM) se identifica estableciendo **ProcessIdentifier** igual a **PROCESSIDTYPE \_ DWM**.</span><span class="sxs-lookup"><span data-stu-id="328c0-119">The Desktop Window Manager (DWM) process is identified by setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="328c0-120">Otros procesos se identifican estableciendo el identificador de proceso en **ProcessHandle** y estableciendo el valor de **ProcessIdentifier** en **PROCESSIDTYPE \_**.</span><span class="sxs-lookup"><span data-stu-id="328c0-120">Other processes are identified by setting the process handle in **ProcessHandle** and setting **ProcessIdentifier** equal to **PROCESSIDTYPE\_HANDLE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="328c0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="328c0-121">Requirements</span></span>



| <span data-ttu-id="328c0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="328c0-122">Requirement</span></span> | <span data-ttu-id="328c0-123">Value</span><span class="sxs-lookup"><span data-stu-id="328c0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="328c0-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="328c0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="328c0-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="328c0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="328c0-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="328c0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="328c0-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="328c0-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="328c0-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="328c0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="328c0-129"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="328c0-129"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="328c0-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="328c0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="328c0-131">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="328c0-131">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="328c0-132">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="328c0-132">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 





---
description: 'Contiene la respuesta del método IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153655"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="1690a-103">D3DAUTHENTICATEDCHANNEL \_ estructura de salida de consulta \_</span><span class="sxs-lookup"><span data-stu-id="1690a-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="1690a-104">Contiene la respuesta del método [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="1690a-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1690a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1690a-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="1690a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1690a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1690a-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="1690a-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="1690a-108">Una estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autentificación de mensajes (Mac) (Mac) de los datos.</span><span class="sxs-lookup"><span data-stu-id="1690a-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="1690a-109">El controlador utiliza una clave CBC MAC (OMAC) basada en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="1690a-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="1690a-110">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="1690a-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="1690a-111">GUID que especifica la consulta.</span><span class="sxs-lookup"><span data-stu-id="1690a-111">A GUID that specifies the query.</span></span> <span data-ttu-id="1690a-112">Para obtener una lista de valores, vea [consultas de Content Protection](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="1690a-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="1690a-113">**ASA**</span><span class="sxs-lookup"><span data-stu-id="1690a-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="1690a-114">Identificador del canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="1690a-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="1690a-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="1690a-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="1690a-116">El número de secuencia de la consulta.</span><span class="sxs-lookup"><span data-stu-id="1690a-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="1690a-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="1690a-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="1690a-118">Código de resultado de la consulta.</span><span class="sxs-lookup"><span data-stu-id="1690a-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1690a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1690a-119">Remarks</span></span>

<span data-ttu-id="1690a-120">En el caso de los miembros **QueryType**, **hChannel** y **SequenceNumber** , el controlador utiliza en los mismos valores que la aplicación proporcionada en la estructura de entrada de la [**\_ \_ consulta D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) .</span><span class="sxs-lookup"><span data-stu-id="1690a-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="1690a-121">La aplicación debe comprobar que estos valores coinciden.</span><span class="sxs-lookup"><span data-stu-id="1690a-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="1690a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1690a-122">Requirements</span></span>



| <span data-ttu-id="1690a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1690a-123">Requirement</span></span> | <span data-ttu-id="1690a-124">Value</span><span class="sxs-lookup"><span data-stu-id="1690a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1690a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1690a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1690a-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="1690a-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1690a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1690a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1690a-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1690a-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1690a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1690a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1690a-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1690a-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1690a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1690a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1690a-132">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="1690a-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="1690a-133">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="1690a-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 





---
description: 'Contiene la respuesta a una llamada al método IDirect3DAuthenticatedChannel9:: configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360106"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a><span data-ttu-id="0b699-103">D3DAUTHENTICATEDCHANNEL \_ configurar la \_ estructura de salida</span><span class="sxs-lookup"><span data-stu-id="0b699-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_OUTPUT structure</span></span>

<span data-ttu-id="0b699-104">Contiene la respuesta a una llamada al método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="0b699-104">Contains the response to a call to the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b699-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b699-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="0b699-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b699-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b699-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="0b699-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="0b699-108">Una estructura [**D3D \_ OMAC**](d3d-omac.md) que contiene un código de autentificación de mensajes (Mac) (Mac) de los datos.</span><span class="sxs-lookup"><span data-stu-id="0b699-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="0b699-109">El controlador utiliza una clave CBC MAC (OMAC) basada en AES para calcular este valor para el bloque de datos que aparece después de este miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="0b699-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="0b699-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="0b699-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="0b699-111">GUID que especifica el comando.</span><span class="sxs-lookup"><span data-stu-id="0b699-111">A GUID that specifies the command.</span></span> <span data-ttu-id="0b699-112">Para obtener una lista de valores, vea [comandos Content Protection](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="0b699-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b699-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="0b699-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="0b699-114">Identificador del canal autenticado.</span><span class="sxs-lookup"><span data-stu-id="0b699-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="0b699-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0b699-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="0b699-116">Número de secuencia del comando.</span><span class="sxs-lookup"><span data-stu-id="0b699-116">The command sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="0b699-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="0b699-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="0b699-118">Código de resultado para el comando.</span><span class="sxs-lookup"><span data-stu-id="0b699-118">The result code for the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b699-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b699-119">Remarks</span></span>

<span data-ttu-id="0b699-120">En el caso de los miembros **ConfigureType**, **hChannel** y **SequenceNumber** , el controlador usa los mismos valores que la aplicación proporcionada en D3DAUTHENTICATEDCHANNEL configurar la estructura de [**\_ \_ entrada**](d3dauthenticatedchannel-configure-input.md) .</span><span class="sxs-lookup"><span data-stu-id="0b699-120">For the **ConfigureType**, **hChannel**, and **SequenceNumber** members, the driver uses the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure.</span></span> <span data-ttu-id="0b699-121">La aplicación debe comprobar que estos valores coinciden.</span><span class="sxs-lookup"><span data-stu-id="0b699-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b699-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b699-122">Requirements</span></span>



| <span data-ttu-id="0b699-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b699-123">Requirement</span></span> | <span data-ttu-id="0b699-124">Value</span><span class="sxs-lookup"><span data-stu-id="0b699-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b699-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b699-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b699-126">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b699-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b699-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b699-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b699-128">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b699-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b699-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b699-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b699-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b699-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b699-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b699-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b699-132">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0b699-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="0b699-133">**IDirect3DAuthenticatedChannel9:: configure**</span><span class="sxs-lookup"><span data-stu-id="0b699-133">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 





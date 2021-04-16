---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE.
ms.assetid: f2e0ae6c-dc97-46f7-933f-6c14d83adf18
title: D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b862523c54dc9f483e63cee525dc61c5f469602d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696152"
---
# <a name="d3dauthenticatedchannel_querydevicehandle_output-structure"></a><span data-ttu-id="36097-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_</span><span class="sxs-lookup"><span data-stu-id="36097-103">D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT structure</span></span>

<span data-ttu-id="36097-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="36097-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) query.</span></span>

<span data-ttu-id="36097-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="36097-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="36097-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36097-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  HANDLE                               DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYDEVICEHANDLE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="36097-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="36097-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="36097-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="36097-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="36097-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="36097-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="36097-110">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="36097-110">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="36097-111">Identificador del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36097-111">A handle to the device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36097-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36097-112">Requirements</span></span>



| <span data-ttu-id="36097-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="36097-113">Requirement</span></span> | <span data-ttu-id="36097-114">Value</span><span class="sxs-lookup"><span data-stu-id="36097-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36097-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36097-115">Minimum supported client</span></span><br/> | <span data-ttu-id="36097-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="36097-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36097-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36097-117">Minimum supported server</span></span><br/> | <span data-ttu-id="36097-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="36097-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36097-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36097-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="36097-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36097-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36097-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="36097-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36097-122">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="36097-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="36097-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="36097-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 





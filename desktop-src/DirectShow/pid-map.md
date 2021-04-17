---
description: La \_ estructura de asignación de PID contiene el contenido de un identificador de paquete de flujo de transporte MPEG-2.
ms.assetid: c247ec75-483d-4587-a82f-07bbf6d277b4
title: PID_MAP estructura (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PID_MAP
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 98b238c61ccfcfb93e4ddcc0a051d9084228f604
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690854"
---
# <a name="pid_map-structure"></a><span data-ttu-id="44774-103">Estructura de asignación de PID \_</span><span class="sxs-lookup"><span data-stu-id="44774-103">PID\_MAP structure</span></span>

<span data-ttu-id="44774-104">La `PID_MAP` estructura contiene identifica el contenido de un identificador de paquete de flujo de transporte MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="44774-104">The `PID_MAP` structure contains identifies the contents of an MPEG-2 transport stream packet ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="44774-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44774-105">Syntax</span></span>


```C++
typedef struct {
  ULONG                ulPID;
  MEDIA_SAMPLE_CONTENT MediaSampleContent;
} PID_MAP;
```



## <a name="members"></a><span data-ttu-id="44774-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="44774-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="44774-107">**ulPID**</span><span class="sxs-lookup"><span data-stu-id="44774-107">**ulPID**</span></span>
</dt> <dd>

<span data-ttu-id="44774-108">Especifica el identificador de paquete (PID)</span><span class="sxs-lookup"><span data-stu-id="44774-108">Specifies the packet ID (PID)</span></span>

</dd> <dt>

<span data-ttu-id="44774-109">**MediaSampleContent**</span><span class="sxs-lookup"><span data-stu-id="44774-109">**MediaSampleContent**</span></span>
</dt> <dd>

<span data-ttu-id="44774-110">Especifica el contenido de la carga de paquete, como un tipo de enumeración de [**\_ \_ contenido de ejemplo multimedia**](media-sample-content.md) .</span><span class="sxs-lookup"><span data-stu-id="44774-110">Specifies the contents of the packet payload, as a [**MEDIA\_SAMPLE\_CONTENT**](media-sample-content.md) enumeration type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44774-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44774-111">Requirements</span></span>



| <span data-ttu-id="44774-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="44774-112">Requirement</span></span> | <span data-ttu-id="44774-113">Value</span><span class="sxs-lookup"><span data-stu-id="44774-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44774-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44774-114">Header</span></span><br/> | <dl> <span data-ttu-id="44774-115"><dt>Bdatypes. h (incluye Bdaiface. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44774-115"><dt>Bdatypes.h (include Bdaiface.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44774-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="44774-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44774-117">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="44774-117">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="44774-118">**Interfaz IEnumPIDMap**</span><span class="sxs-lookup"><span data-stu-id="44774-118">**IEnumPIDMap Interface**</span></span>](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-ienumpidmap)
</dt> </dl>

 

 





---
description: Contiene un código de autentificación de mensajes (MAC) (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: D3D_OMAC estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720298"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="36216-103">\_Estructura OMAC de D3D</span><span class="sxs-lookup"><span data-stu-id="36216-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="36216-104">Contiene un código de autentificación de mensajes (MAC) (MAC).</span><span class="sxs-lookup"><span data-stu-id="36216-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="36216-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36216-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="36216-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="36216-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="36216-107">**Omac**</span><span class="sxs-lookup"><span data-stu-id="36216-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="36216-108">Matriz de bytes que contiene el valor de MAC criptográfico del mensaje.</span><span class="sxs-lookup"><span data-stu-id="36216-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="36216-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36216-109">Requirements</span></span>



| <span data-ttu-id="36216-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="36216-110">Requirement</span></span> | <span data-ttu-id="36216-111">Value</span><span class="sxs-lookup"><span data-stu-id="36216-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36216-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36216-112">Minimum supported client</span></span><br/> | <span data-ttu-id="36216-113">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="36216-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36216-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36216-114">Minimum supported server</span></span><br/> | <span data-ttu-id="36216-115">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="36216-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36216-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36216-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="36216-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="36216-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36216-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="36216-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36216-119">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="36216-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 





---
title: MCI_PLAY_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura de parms de reproducción de MCI contiene información de posicionamiento del comando de reproducción de MCI \_ .
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- Estructura de MCI_PLAY_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995913"
---
# <a name="mci_play_parms-structure"></a><span data-ttu-id="d3ce3-104">\_Estructura parms de reproducción de MCI \_</span><span class="sxs-lookup"><span data-stu-id="d3ce3-104">MCI\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="d3ce3-105">La estructura de **\_ \_ parms de reproducción de MCI** contiene información de posicionamiento del comando de [**\_ reproducción de MCI**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="d3ce3-105">The **MCI\_PLAY\_PARMS** structure contains positioning information for the [**MCI\_PLAY**](mci-play.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ce3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3ce3-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="d3ce3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d3ce3-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3ce3-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d3ce3-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="d3ce3-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d3ce3-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="d3ce3-111">Posición desde la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="d3ce3-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="d3ce3-113">Posición en la que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3ce3-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3ce3-114">Remarks</span></span>

<span data-ttu-id="d3ce3-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ce3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3ce3-116">Requirements</span></span>



| <span data-ttu-id="d3ce3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ce3-117">Requirement</span></span> | <span data-ttu-id="d3ce3-118">Value</span><span class="sxs-lookup"><span data-stu-id="d3ce3-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ce3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3ce3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ce3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3ce3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d3ce3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3ce3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ce3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3ce3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3ce3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3ce3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3ce3-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3ce3-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3ce3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3ce3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ce3-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d3ce3-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d3ce3-128">**reproducción de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="d3ce3-128">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="d3ce3-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3ce3-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


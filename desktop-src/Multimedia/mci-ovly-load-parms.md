---
title: Estructura de MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: La \_ estructura MCI OVLY \_ Load \_ parms contiene información del comando de carga de MCI \_ para dispositivos de superposición de vídeo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Estructura de MCI_OVLY_LOAD_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078842"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="1753c-104">La \_ estructura de parms de MCI OVLY \_ Load \_</span><span class="sxs-lookup"><span data-stu-id="1753c-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="1753c-105">La estructura **MCI \_ OVLY \_ Load \_ parms** contiene información del comando de [**\_ carga de MCI**](mci-load.md) para dispositivos de superposición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1753c-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="1753c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1753c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="1753c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1753c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1753c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="1753c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1753c-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="1753c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="1753c-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="1753c-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="1753c-111">Nombre del archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="1753c-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="1753c-112">**CR**</span><span class="sxs-lookup"><span data-stu-id="1753c-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="1753c-113">Identifica el área del búfer de vídeo que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="1753c-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="1753c-114">Las estructuras [Rect](/previous-versions//ms536136(v=vs.85)) se administran de forma diferente en MCI que en otras partes de Windows. en MCI, **RC. Right** contiene el ancho del rectángulo y **RC. Bottom** contiene el alto.</span><span class="sxs-lookup"><span data-stu-id="1753c-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1753c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1753c-115">Remarks</span></span>

<span data-ttu-id="1753c-116">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="1753c-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="1753c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1753c-117">Requirements</span></span>



| <span data-ttu-id="1753c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1753c-118">Requirement</span></span> | <span data-ttu-id="1753c-119">Value</span><span class="sxs-lookup"><span data-stu-id="1753c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1753c-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1753c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1753c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1753c-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1753c-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1753c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1753c-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1753c-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1753c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1753c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1753c-125"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="1753c-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1753c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1753c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1753c-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="1753c-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1753c-128">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="1753c-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="1753c-129">**carga de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="1753c-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="1753c-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1753c-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1753c-131">[RECT](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1753c-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 


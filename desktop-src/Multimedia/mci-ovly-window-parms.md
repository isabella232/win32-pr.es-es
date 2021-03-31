---
title: MCI_OVLY_WINDOW_PARMS estructura (Mciapi. h)
description: La \_ estructura parms de la ventana de OVLY MCI \_ \_ contiene información de visualización de ventana para el comando de la \_ ventana MCI para dispositivos de superposición de vídeo.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Estructura de MCI_OVLY_WINDOW_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995914"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="34508-104">\_Estructura parms de la ventana de OVLY MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="34508-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="34508-105">La estructura parms de la **\_ ventana de OVLY \_ \_ MCI** contiene información de visualización de ventana para el comando de la [**\_ ventana MCI**](mci-window.md) para dispositivos de superposición de vídeo.</span><span class="sxs-lookup"><span data-stu-id="34508-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="34508-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34508-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="34508-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="34508-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="34508-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="34508-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="34508-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="34508-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="34508-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="34508-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="34508-111">Identificador de la ventana de presentación.</span><span class="sxs-lookup"><span data-stu-id="34508-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="34508-112">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="34508-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="34508-113">Comando de visualización de ventana.</span><span class="sxs-lookup"><span data-stu-id="34508-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="34508-114">**lpstrText**</span><span class="sxs-lookup"><span data-stu-id="34508-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="34508-115">Título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="34508-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34508-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34508-116">Remarks</span></span>

<span data-ttu-id="34508-117">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="34508-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="34508-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34508-118">Requirements</span></span>



| <span data-ttu-id="34508-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="34508-119">Requirement</span></span> | <span data-ttu-id="34508-120">Value</span><span class="sxs-lookup"><span data-stu-id="34508-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34508-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34508-121">Minimum supported client</span></span><br/> | <span data-ttu-id="34508-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="34508-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="34508-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34508-123">Minimum supported server</span></span><br/> | <span data-ttu-id="34508-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="34508-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="34508-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34508-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="34508-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="34508-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34508-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="34508-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34508-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="34508-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="34508-129">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="34508-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="34508-130">**\_ventana MCI**</span><span class="sxs-lookup"><span data-stu-id="34508-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="34508-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="34508-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


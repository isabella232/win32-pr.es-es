---
title: MCI_VCR_SEEK_PARMS estructura (VCR. h)
description: La \_ estructura de parms de VCR VCR \_ Seek \_ contiene los parámetros para el \_ comando MCI Seek para los grabadores de casete de vídeo.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- Estructura de MCI_VCR_SEEK_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489898"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="165c9-104">\_Estructura parms de VCR VCR \_ Seek \_</span><span class="sxs-lookup"><span data-stu-id="165c9-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="165c9-105">La estructura de **\_ parms de VCR VCR \_ Seek \_** contiene los parámetros para el comando [**MCI \_ Seek**](mci-seek.md) para los grabadores de casete de vídeo.</span><span class="sxs-lookup"><span data-stu-id="165c9-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="165c9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="165c9-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="165c9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="165c9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="165c9-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="165c9-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="165c9-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="165c9-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="165c9-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="165c9-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="165c9-111">Posición en la que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="165c9-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="165c9-112">**dwMark**</span><span class="sxs-lookup"><span data-stu-id="165c9-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="165c9-113">Marca numerada que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="165c9-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="165c9-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="165c9-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="165c9-115">Hora a la que comienza la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="165c9-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="165c9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="165c9-116">Remarks</span></span>

<span data-ttu-id="165c9-117">Las posiciones se especifican en el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="165c9-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="165c9-118">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="165c9-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="165c9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="165c9-119">Requirements</span></span>



| <span data-ttu-id="165c9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="165c9-120">Requirement</span></span> | <span data-ttu-id="165c9-121">Value</span><span class="sxs-lookup"><span data-stu-id="165c9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="165c9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="165c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="165c9-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="165c9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="165c9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="165c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="165c9-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="165c9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="165c9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="165c9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="165c9-127"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="165c9-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165c9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="165c9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165c9-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="165c9-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="165c9-130">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="165c9-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="165c9-131">**búsqueda de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="165c9-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="165c9-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="165c9-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


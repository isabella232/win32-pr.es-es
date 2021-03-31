---
title: MCI_SEEK_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura de parms de búsqueda de MCI contiene información de posicionamiento para el \_ comando MCI Seek.
ms.assetid: 2c199855-2134-4709-9313-5b8d66ce4f03
keywords:
- Estructura de MCI_SEEK_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SEEK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c31f419b2458dedc19c6533e8f0f7fade97026e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801514"
---
# <a name="mci_seek_parms-structure"></a><span data-ttu-id="ec36a-104">\_Estructura parms de búsqueda de MCI \_</span><span class="sxs-lookup"><span data-stu-id="ec36a-104">MCI\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="ec36a-105">La estructura de **\_ \_ parms de búsqueda de MCI** contiene información de posicionamiento para el comando [**MCI \_ Seek**](mci-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="ec36a-105">The **MCI\_SEEK\_PARMS** structure contains positioning information for the [**MCI\_SEEK**](mci-seek.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec36a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec36a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
} MCI_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="ec36a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec36a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec36a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="ec36a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="ec36a-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="ec36a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="ec36a-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="ec36a-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="ec36a-111">Posición en la que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="ec36a-111">Position to seek to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec36a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec36a-112">Remarks</span></span>

<span data-ttu-id="ec36a-113">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="ec36a-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec36a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec36a-114">Requirements</span></span>



| <span data-ttu-id="ec36a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec36a-115">Requirement</span></span> | <span data-ttu-id="ec36a-116">Value</span><span class="sxs-lookup"><span data-stu-id="ec36a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ec36a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec36a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ec36a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ec36a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ec36a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec36a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ec36a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec36a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ec36a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec36a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec36a-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec36a-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec36a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec36a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec36a-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="ec36a-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ec36a-125">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="ec36a-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="ec36a-126">**búsqueda de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="ec36a-126">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="ec36a-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec36a-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


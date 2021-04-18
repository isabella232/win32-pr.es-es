---
title: MCI_VD_ESCAPE_PARMS estructura (Mciapi. h)
description: La estructura parms de los caracteres de escape de MCI \_ Vd \_ \_ contiene el comando que se envía a un dispositivo para el \_ comando MCI escape para dispositivos de VideoDisc.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- Estructura de MCI_VD_ESCAPE_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676717"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="2f7dd-104">\_ \_ Estructura parms de secuencias de escape de MCI Vd \_</span><span class="sxs-lookup"><span data-stu-id="2f7dd-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="2f7dd-105">La **estructura \_ \_ \_ parms** de los caracteres de escape de MCI Vd contiene el comando que se envía a un dispositivo para el comando [**MCI \_ escape**](mci-escape.md) para dispositivos de VideoDisc.</span><span class="sxs-lookup"><span data-stu-id="2f7dd-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7dd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f7dd-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="2f7dd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f7dd-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f7dd-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="2f7dd-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="2f7dd-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="2f7dd-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="2f7dd-110">**lpstrCommand**</span><span class="sxs-lookup"><span data-stu-id="2f7dd-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="2f7dd-111">Comando que se va a enviar a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f7dd-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f7dd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f7dd-112">Remarks</span></span>

<span data-ttu-id="2f7dd-113">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="2f7dd-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7dd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7dd-114">Requirements</span></span>



| <span data-ttu-id="2f7dd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7dd-115">Requirement</span></span> | <span data-ttu-id="2f7dd-116">Value</span><span class="sxs-lookup"><span data-stu-id="2f7dd-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7dd-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f7dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7dd-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2f7dd-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2f7dd-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f7dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7dd-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f7dd-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f7dd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f7dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f7dd-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f7dd-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7dd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f7dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7dd-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="2f7dd-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="2f7dd-125">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="2f7dd-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="2f7dd-126">**ESCAPE de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="2f7dd-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="2f7dd-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f7dd-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


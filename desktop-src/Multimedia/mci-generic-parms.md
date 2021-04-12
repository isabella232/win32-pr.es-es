---
title: MCI_GENERIC_PARMS estructura (Mciapi. h)
description: La \_ \_ estructura parms genérica de MCI contiene el identificador de la ventana que recibe los mensajes de notificación. Esta estructura se usa para los mensajes de comandos MCI que tienen listas de parámetros vacías.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Estructura de MCI_GENERIC_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490121"
---
# <a name="mci_generic_parms-structure"></a><span data-ttu-id="718d4-105">\_Estructura parms genérica de MCI \_</span><span class="sxs-lookup"><span data-stu-id="718d4-105">MCI\_GENERIC\_PARMS structure</span></span>

<span data-ttu-id="718d4-106">La **estructura \_ \_ parms genérica de MCI** contiene el identificador de la ventana que recibe los mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="718d4-106">The **MCI\_GENERIC\_PARMS** structure contains the handle of the window that receives notification messages.</span></span> <span data-ttu-id="718d4-107">Esta estructura se usa para los mensajes de comandos MCI que tienen listas de parámetros vacías.</span><span class="sxs-lookup"><span data-stu-id="718d4-107">This structure is used for MCI command messages that have empty parameter lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="718d4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="718d4-108">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a><span data-ttu-id="718d4-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="718d4-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="718d4-110">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="718d4-110">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="718d4-111">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="718d4-111">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="718d4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="718d4-112">Remarks</span></span>

<span data-ttu-id="718d4-113">Las estructuras **MCI \_ Close \_ parms** y **MCI \_ observan \_ parms** son idénticas a la estructura **\_ \_ parms de MCI genérica** .</span><span class="sxs-lookup"><span data-stu-id="718d4-113">The **MCI\_CLOSE\_PARMS** and **MCI\_REALIZE\_PARMS** structures are identical to the **MCI\_GENERIC\_PARMS** structure.</span></span>

<span data-ttu-id="718d4-114">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="718d4-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="718d4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="718d4-115">Requirements</span></span>



| <span data-ttu-id="718d4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="718d4-116">Requirement</span></span> | <span data-ttu-id="718d4-117">Value</span><span class="sxs-lookup"><span data-stu-id="718d4-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="718d4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718d4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="718d4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="718d4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="718d4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718d4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="718d4-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="718d4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="718d4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="718d4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="718d4-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="718d4-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="718d4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="718d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718d4-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="718d4-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="718d4-126">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="718d4-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

<span data-ttu-id="718d4-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="718d4-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


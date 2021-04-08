---
title: Estructura de MCI_LOAD_PARMS (mmsystem. h)
description: La \_ estructura de parms de carga de MCI \_ contiene el nombre de archivo que se va a cargar para el \_ comando MCI Load.
ms.assetid: 371d11cc-44db-496b-b51a-66d7b919b794
keywords:
- Estructura de MCI_LOAD_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04697a52eb9f8bb33db6063eb47e791be674f1d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803361"
---
# <a name="mci_load_parms-structure"></a><span data-ttu-id="6c60b-104">\_Estructura parms de carga de MCI \_</span><span class="sxs-lookup"><span data-stu-id="6c60b-104">MCI\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="6c60b-105">La estructura de **\_ \_ parms de carga de MCI** contiene el nombre de archivo que se va a cargar para el comando [**MCI \_ Load**](mci-load.md) .</span><span class="sxs-lookup"><span data-stu-id="6c60b-105">The **MCI\_LOAD\_PARMS** structure contains the filename to load for the [**MCI\_LOAD**](mci-load.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c60b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c60b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="6c60b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c60b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6c60b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="6c60b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="6c60b-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="6c60b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="6c60b-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="6c60b-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="6c60b-111">Nombre del archivo que se va a cargar.</span><span class="sxs-lookup"><span data-stu-id="6c60b-111">Name of file to load.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c60b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c60b-112">Remarks</span></span>

<span data-ttu-id="6c60b-113">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="6c60b-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c60b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c60b-114">Requirements</span></span>



| <span data-ttu-id="6c60b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c60b-115">Requirement</span></span> | <span data-ttu-id="6c60b-116">Value</span><span class="sxs-lookup"><span data-stu-id="6c60b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c60b-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c60b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c60b-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6c60b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6c60b-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c60b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c60b-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c60b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c60b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c60b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c60b-122"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c60b-122"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c60b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c60b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c60b-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="6c60b-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6c60b-125">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="6c60b-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="6c60b-126">**carga de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="6c60b-126">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="6c60b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6c60b-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


---
title: MCI_SAVE_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI Save \_ parms contiene la información del nombre de archivo para el \_ comando MCI Save.
ms.assetid: fbaff175-e521-4b93-853a-f444726932d3
keywords:
- Estructura de MCI_SAVE_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SAVE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6252788b1ffc251d2fa6a3f993f074edc31aaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676625"
---
# <a name="mci_save_parms-structure"></a><span data-ttu-id="0b0e1-104">MCI \_ Save \_ parms Structure</span><span class="sxs-lookup"><span data-stu-id="0b0e1-104">MCI\_SAVE\_PARMS structure</span></span>

<span data-ttu-id="0b0e1-105">La estructura **MCI \_ Save \_ parms** contiene la información del nombre de archivo para el comando [**MCI \_ Save**](mci-save.md) .</span><span class="sxs-lookup"><span data-stu-id="0b0e1-105">The **MCI\_SAVE\_PARMS** structure contains the filename information for the [**MCI\_SAVE**](mci-save.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0e1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b0e1-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
} MCI_SAVE_PARMS;
```



## <a name="members"></a><span data-ttu-id="0b0e1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b0e1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0b0e1-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="0b0e1-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0b0e1-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="0b0e1-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0b0e1-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="0b0e1-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="0b0e1-111">Nombre del archivo que se va a guardar.</span><span class="sxs-lookup"><span data-stu-id="0b0e1-111">Name of file to save.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b0e1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b0e1-112">Remarks</span></span>

<span data-ttu-id="0b0e1-113">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="0b0e1-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b0e1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b0e1-114">Requirements</span></span>



| <span data-ttu-id="0b0e1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b0e1-115">Requirement</span></span> | <span data-ttu-id="0b0e1-116">Value</span><span class="sxs-lookup"><span data-stu-id="0b0e1-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0b0e1-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b0e1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0b0e1-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0b0e1-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0b0e1-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b0e1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0b0e1-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b0e1-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0b0e1-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b0e1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b0e1-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b0e1-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b0e1-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b0e1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b0e1-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0b0e1-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0b0e1-125">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="0b0e1-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0b0e1-126">**\_Guardar MCI**</span><span class="sxs-lookup"><span data-stu-id="0b0e1-126">**MCI\_SAVE**</span></span>](mci-save.md)
</dt> <dt>

<span data-ttu-id="0b0e1-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b0e1-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


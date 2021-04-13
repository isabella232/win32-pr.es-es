---
title: MCI_INFO_PARMS estructura (Mciapi. h)
description: La \_ estructura MCI info \_ parms contiene información del comando MCI \_ info.
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- Estructura de MCI_INFO_PARMS de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493036"
---
# <a name="mci_info_parms-structure"></a><span data-ttu-id="c50e0-104">Estructura de parms de \_ información de MCI \_</span><span class="sxs-lookup"><span data-stu-id="c50e0-104">MCI\_INFO\_PARMS structure</span></span>

<span data-ttu-id="c50e0-105">La estructura **MCI \_ info \_ parms** contiene información del comando [**MCI \_ info**](mci-info.md) .</span><span class="sxs-lookup"><span data-stu-id="c50e0-105">The **MCI\_INFO\_PARMS** structure contains information for the [**MCI\_INFO**](mci-info.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50e0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c50e0-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="c50e0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c50e0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c50e0-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c50e0-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c50e0-109">La palabra de orden inferior especifica un identificador de ventana que se usa para la marca de notificación de MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="c50e0-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c50e0-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="c50e0-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="c50e0-111">Búfer de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="c50e0-111">Buffer for return string.</span></span>

</dd> <dt>

<span data-ttu-id="c50e0-112">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="c50e0-112">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="c50e0-113">Tamaño, en caracteres, de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="c50e0-113">Size, in characters, of return string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c50e0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c50e0-114">Remarks</span></span>

<span data-ttu-id="c50e0-115">Al asignar datos a los miembros de esta estructura, establezca las marcas correspondientes en el parámetro *fdwCommand* de la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar los miembros.</span><span class="sxs-lookup"><span data-stu-id="c50e0-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c50e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c50e0-116">Requirements</span></span>



| <span data-ttu-id="c50e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c50e0-117">Requirement</span></span> | <span data-ttu-id="c50e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="c50e0-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c50e0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c50e0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c50e0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c50e0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c50e0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c50e0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c50e0-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c50e0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c50e0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c50e0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50e0-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50e0-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50e0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c50e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50e0-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c50e0-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c50e0-127">**Estructuras de MCI**</span><span class="sxs-lookup"><span data-stu-id="c50e0-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c50e0-128">**información de MCI \_**</span><span class="sxs-lookup"><span data-stu-id="c50e0-128">**MCI\_INFO**</span></span>](mci-info.md)
</dt> <dt>

<span data-ttu-id="c50e0-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c50e0-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 


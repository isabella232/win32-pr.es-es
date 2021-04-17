---
title: Mensaje de LVM_SETINFOTIP (commctrl. h)
description: Establece el texto de información sobre herramientas en respuesta diferida en la notificación de GETINFOTIP de LVN \_ .
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- LVM_SETINFOTIP controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656467"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="1b1da-104">\_Mensaje SETINFOTIP LVM</span><span class="sxs-lookup"><span data-stu-id="1b1da-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="1b1da-105">Establece el texto de información sobre herramientas en respuesta diferida en la notificación de [ \_ GETINFOTIP de LVN](lvn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="1b1da-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="1b1da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b1da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b1da-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1b1da-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1b1da-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1b1da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b1da-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1b1da-110">Puntero a una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> que contiene la información que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="1b1da-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1da-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b1da-111">Return value</span></span>

<span data-ttu-id="1b1da-112">Devuelve **true** si el texto de información sobre herramientas se establece correctamente, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1b1da-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b1da-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b1da-113">Remarks</span></span>

<span data-ttu-id="1b1da-114">El mensaje **LVM \_ SETINFOTIP** permite a una aplicación calcular recuadros informativos en segundo plano realizando los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1b1da-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="1b1da-115">En respuesta a la notificación de [ \_ GETINFOTIP de LVN](lvn-getinfotip.md) , establezca el miembro **miembros pszText** de la estructura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) en una cadena vacía y devuelva 0.</span><span class="sxs-lookup"><span data-stu-id="1b1da-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="1b1da-116">En segundo plano, calcule el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="1b1da-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="1b1da-117">Después de calcular el recuadro informativo, envíe el mensaje **LVM \_ SETINFOTIP** , estableciendo el miembro **miembros pszText** de la estructura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) en el elemento recuadro informativo y los miembros **iItem** y **iSubItem** en el elemento y el subelemento al que se aplica el recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="1b1da-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="1b1da-118">El texto que se pasa al mensaje **LVM \_ SETINFOTIP** solo aparece si el elemento y el subelemento descritos por la estructura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) siguen en un estado que requiere un recuadro informativo</span><span class="sxs-lookup"><span data-stu-id="1b1da-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="1b1da-119">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="1b1da-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1b1da-120">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1b1da-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b1da-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b1da-121">Requirements</span></span>



| <span data-ttu-id="1b1da-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b1da-122">Requirement</span></span> | <span data-ttu-id="1b1da-123">Value</span><span class="sxs-lookup"><span data-stu-id="1b1da-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1da-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b1da-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1da-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="1b1da-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b1da-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b1da-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1da-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b1da-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b1da-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b1da-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b1da-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b1da-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






---
title: Mensaje de LVM_SETGROUPINFO (commctrl. h)
description: Establece la información del grupo.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 688c5b56a57a579e5955fa62a9b44d88258b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078862"
---
# <a name="lvm_setgroupinfo-message"></a><span data-ttu-id="f0cde-104">\_Mensaje SETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="f0cde-104">LVM\_SETGROUPINFO message</span></span>

<span data-ttu-id="f0cde-105">Establece la información del grupo.</span><span class="sxs-lookup"><span data-stu-id="f0cde-105">Sets group information.</span></span> <span data-ttu-id="f0cde-106">Envíe este mensaje explícitamente o mediante la [**macro \_ SetGroupInfo de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) .</span><span class="sxs-lookup"><span data-stu-id="f0cde-106">Send this message explicitly or by using the [**ListView\_SetGroupInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0cde-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0cde-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0cde-108">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-108">*wParam* \[in\]</span></span>
</dt> <dd><span data-ttu-id="f0cde-109">IDENTIFICADOR que especifica el grupo cuya información se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f0cde-109">ID that specifies the group whose information is to be set.</span></span></dd> <dt>

<span data-ttu-id="f0cde-110">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-110">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="f0cde-111">Puntero a una estructura [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) que contiene la información que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="f0cde-111">Pointer to a [**LVGROUP**](windows/win32/api/commctrl/ns-commctrl-lvgroup) structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0cde-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0cde-112">Return value</span></span>

<span data-ttu-id="f0cde-113">Devuelve el identificador del grupo si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f0cde-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0cde-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0cde-114">Remarks</span></span>

<span data-ttu-id="f0cde-115">Para cambiar el identificador de un grupo existente, agregue <b>LVGF_GROUPID</b> a <b>LVGROUP. Mask</b> y establezca <b>LVGROUP. iGroupId</b> en el nuevo identificador.</span><span class="sxs-lookup"><span data-stu-id="f0cde-115">To change a group ID of an existing group add <b>LVGF_GROUPID</b> to <b>LVGROUP.mask</b> and set <b>LVGROUP.iGroupId</b> to the new ID.</span></span> <span data-ttu-id="f0cde-116">Se producirá un error en la llamada si <b>LVGROUP. iGroupId</b> contiene el identificador de un grupo existente.</span><span class="sxs-lookup"><span data-stu-id="f0cde-116">The call will fail if <b>LVGROUP.iGroupId</b> contains ID of an existing group.</span></span>

<span data-ttu-id="f0cde-117">Para actualizar otras propiedades de un grupo existente (por ejemplo, actualizar una alineación del texto del encabezado o del pie de página del grupo, <b>uAlign</b>) <b>LVGROUP. Mask</b> no debe contener <b>LVGF_GROUPID</b>. de lo contrario, se producirá un error en la actualización.</span><span class="sxs-lookup"><span data-stu-id="f0cde-117">To update other properties of an existing group (e.g. update an alignment of the header or footer text for the group, <b>uAlign</b>) <b>LVGROUP.mask</b> must not contain <b>LVGF_GROUPID</b>, else the update will fail.</span></span>

> [!Note]  
> <span data-ttu-id="f0cde-118">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="f0cde-118">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f0cde-119">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f0cde-119">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0cde-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0cde-120">Requirements</span></span>



| <span data-ttu-id="f0cde-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0cde-121">Requirement</span></span> | <span data-ttu-id="f0cde-122">Value</span><span class="sxs-lookup"><span data-stu-id="f0cde-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cde-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0cde-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f0cde-124">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0cde-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0cde-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f0cde-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0cde-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0cde-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0cde-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0cde-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0cde-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






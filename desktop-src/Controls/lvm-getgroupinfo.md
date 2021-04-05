---
title: Mensaje de LVM_GETGROUPINFO (commctrl. h)
description: Obtiene la información del grupo.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079205"
---
# <a name="lvm_getgroupinfo-message"></a><span data-ttu-id="9b64e-104">\_Mensaje GETGROUPINFO LVM</span><span class="sxs-lookup"><span data-stu-id="9b64e-104">LVM\_GETGROUPINFO message</span></span>

<span data-ttu-id="9b64e-105">Obtiene la información del grupo.</span><span class="sxs-lookup"><span data-stu-id="9b64e-105">Gets group information.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b64e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b64e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b64e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b64e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9b64e-108">IDENTIFICADOR que especifica el grupo cuya información se recupera.</span><span class="sxs-lookup"><span data-stu-id="9b64e-108">An ID that specifies the group whose information is retrieved.</span></span></dd> <dt>

<span data-ttu-id="9b64e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b64e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9b64e-110">Puntero A una estructura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que recibe la información recuperada.</span><span class="sxs-lookup"><span data-stu-id="9b64e-110">A pointer an <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that receives the retrieved information.</span></span> <span data-ttu-id="9b64e-111">Establezca el miembro **cbSize** de esta estructura en SIZEOF (LVGROUP).</span><span class="sxs-lookup"><span data-stu-id="9b64e-111">Set the **cbSize** member of this structure to sizeof(LVGROUP).</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b64e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b64e-112">Return value</span></span>

<span data-ttu-id="9b64e-113">Devuelve el identificador del grupo si se realiza correctamente, o-1 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9b64e-113">Returns the ID of the group if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b64e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b64e-114">Remarks</span></span>

<span data-ttu-id="9b64e-115">Antes de intentar recuperar el encabezado de un grupo, asegúrese primero de que el grupo no tenga el \_ estilo NOheader LBGS.</span><span class="sxs-lookup"><span data-stu-id="9b64e-115">Before attempting to retrieve the header for a group, first ensure that the group does not have the LBGS\_NOHEADER style.</span></span>

> [!Note]  
> <span data-ttu-id="9b64e-116">Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0.</span><span class="sxs-lookup"><span data-stu-id="9b64e-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="9b64e-117">Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9b64e-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9b64e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b64e-118">Requirements</span></span>



| <span data-ttu-id="9b64e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b64e-119">Requirement</span></span> | <span data-ttu-id="9b64e-120">Value</span><span class="sxs-lookup"><span data-stu-id="9b64e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b64e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b64e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9b64e-122">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9b64e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b64e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b64e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9b64e-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b64e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b64e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b64e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b64e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b64e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 






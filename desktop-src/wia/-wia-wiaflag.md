---
description: 'Marcas usadas por los métodos IWiaDevMgr:: GetImageDlg, IWiaDevMgr2:: GetImageDlg, IWiaItem::D eviceDlg y IWiaItem2::D eviceDlg para controlar la operación del cuadro de diálogo.'
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659805"
---
# <a name="wiaflag"></a><span data-ttu-id="9dcc4-103">WiaFlag</span><span class="sxs-lookup"><span data-stu-id="9dcc4-103">WiaFlag</span></span>

<span data-ttu-id="9dcc4-104">Marcas usadas por los métodos [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)y [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) para controlar la operación del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9dcc4-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="9dcc4-105">Constante</span><span class="sxs-lookup"><span data-stu-id="9dcc4-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="9dcc4-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dcc4-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="9dcc4-107"><dt>**\_cuadro de diálogo de dispositivo WIA \_ \_ \_ imagen única**</dt></span><span class="sxs-lookup"><span data-stu-id="9dcc4-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="9dcc4-108">Restrinja la selección de imágenes a una sola imagen en el cuadro de diálogo adquisición de imagen de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dcc4-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="9dcc4-109"><dt>**cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común**</dt></span><span class="sxs-lookup"><span data-stu-id="9dcc4-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="9dcc4-110">Use la interfaz de usuario del sistema, si está disponible, en lugar de la interfaz de usuario proporcionada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="9dcc4-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="9dcc4-111">Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor.</span><span class="sxs-lookup"><span data-stu-id="9dcc4-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="9dcc4-112">Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="9dcc4-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="9dcc4-113"><dt>**WIA \_ seleccionar \_ dispositivo \_ predeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="9dcc4-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="9dcc4-114">Fuerce el método [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) o [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) para mostrar el cuadro de diálogo **seleccionar dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="9dcc4-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9dcc4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dcc4-115">Requirements</span></span>



| <span data-ttu-id="9dcc4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dcc4-116">Requirement</span></span> | <span data-ttu-id="9dcc4-117">Value</span><span class="sxs-lookup"><span data-stu-id="9dcc4-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9dcc4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dcc4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9dcc4-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9dcc4-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9dcc4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dcc4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9dcc4-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9dcc4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9dcc4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dcc4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dcc4-123"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dcc4-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 





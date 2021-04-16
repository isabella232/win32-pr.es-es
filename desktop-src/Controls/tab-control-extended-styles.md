---
title: Estilos extendidos del control de pestaña (CommCtrl. h)
description: El control de pestaña ahora admite estilos extendidos. Estos estilos se manipulan mediante los \_ mensajes TCM GETEXTENDEDSTYLE y TCM \_ SETEXTENDEDSTYLE y no se deben confundir con los estilos de ventana extendidos que se pasan a CreateWindowEx.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649771"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="fd9be-104">Estilos extendidos del control de pestaña</span><span class="sxs-lookup"><span data-stu-id="fd9be-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="fd9be-105">El control de pestaña ahora admite estilos extendidos.</span><span class="sxs-lookup"><span data-stu-id="fd9be-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="fd9be-106">Estos estilos se manipulan mediante los mensajes [**TCM \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) y [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) y no se deben confundir con los estilos de ventana extendidos que se pasan a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span><span class="sxs-lookup"><span data-stu-id="fd9be-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="fd9be-107">Constante</span><span class="sxs-lookup"><span data-stu-id="fd9be-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="fd9be-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd9be-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="fd9be-109"><dt>**ECT \_ ex \_ FLATSEPARATORS**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9be-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="fd9be-110">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="fd9be-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="fd9be-111">El control de pestaña dibujará separadores entre los elementos de ficha.</span><span class="sxs-lookup"><span data-stu-id="fd9be-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="fd9be-112">Este estilo extendido solo afecta a los controles de ficha que tienen los [**\_ botones de TCS**](tab-control-styles.md) y los estilos de [**\_ FLATBUTTONS de TCS**](tab-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fd9be-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="fd9be-113">De forma predeterminada, al crear el control de pestaña con el estilo **TCS \_ FLATBUTTONS** se establece este estilo extendido.</span><span class="sxs-lookup"><span data-stu-id="fd9be-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="fd9be-114">Si no necesita separadores, debe quitar este estilo extendido después de crear el control.</span><span class="sxs-lookup"><span data-stu-id="fd9be-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="fd9be-115"><dt>**ECT \_ ex \_ REGISTERDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="fd9be-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="fd9be-116">[Versión 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="fd9be-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="fd9be-117">El control de pestaña genera códigos de notificación [TCN \_ GETOBJECT](tcn-getobject.md) para solicitar un objeto de destino de colocación cuando se arrastra un objeto sobre los elementos de ficha del control.</span><span class="sxs-lookup"><span data-stu-id="fd9be-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="fd9be-118">La aplicación debe llamar a [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) o [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) antes de establecer este estilo.</span><span class="sxs-lookup"><span data-stu-id="fd9be-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="fd9be-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd9be-119">Requirements</span></span>



| <span data-ttu-id="fd9be-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd9be-120">Requirement</span></span> | <span data-ttu-id="fd9be-121">Value</span><span class="sxs-lookup"><span data-stu-id="fd9be-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd9be-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd9be-122">Header</span></span><br/> | <dl> <span data-ttu-id="fd9be-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd9be-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 


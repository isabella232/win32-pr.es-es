---
title: Métodos de ID2D1Device CreatePrintControl (D2d1 \_ 1. h)
description: Crea un objeto ID2D1PrintControl que convierte los primitivos de Direct2D almacenados en ID2D1CommandList en una representación de página fija. A continuación, el subsistema de impresión usa los primitivos.
ms.assetid: C8860AEE-807A-435E-9F44-B50545320EDA
keywords:
- Métodos de CreatePrintControl Direct2D
topic_type:
- apiref
api_location:
- d2d1_1.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ec8705d73f40fc967b3247aaf81caebcade47b02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679044"
---
# <a name="id2d1devicecreateprintcontrol-methods"></a><span data-ttu-id="2de22-105">ID2D1Device:: CreatePrintControl (métodos)</span><span class="sxs-lookup"><span data-stu-id="2de22-105">ID2D1Device::CreatePrintControl methods</span></span>

<span data-ttu-id="2de22-106">Crea un objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) que convierte los primitivos de [Direct2D](/windows/desktop/direct2d/direct2d-portal) almacenados en [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) en una representación de página fija.</span><span class="sxs-lookup"><span data-stu-id="2de22-106">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="2de22-107">A continuación, el subsistema de impresión usa los primitivos.</span><span class="sxs-lookup"><span data-stu-id="2de22-107">The print sub-system then consumes the primitives.</span></span>

### <a name="overload-list"></a><span data-ttu-id="2de22-108">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="2de22-108">Overload list</span></span>



| <span data-ttu-id="2de22-109">Método</span><span class="sxs-lookup"><span data-stu-id="2de22-109">Method</span></span>                                                                                                                                                                           | <span data-ttu-id="2de22-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2de22-110">Description</span></span>                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de22-111">[**CreatePrintControl (IWICImagingFactory \* , IPrintDocumentPackageTarget \* , D2D1 \_ \_ \_ propiedades de control \* de impresión, ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="2de22-111">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES\*, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties_id2d1printcontrol))</span></span> | <span data-ttu-id="2de22-112">Crea un objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) que convierte los primitivos de [Direct2D](/windows/desktop/direct2d/direct2d-portal) almacenados en [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) en una representación de página fija.</span><span class="sxs-lookup"><span data-stu-id="2de22-112">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="2de22-113">A continuación, el subsistema de impresión usa los primitivos.</span><span class="sxs-lookup"><span data-stu-id="2de22-113">The print sub-system then consumes the primitives.</span></span><br/> |
| <span data-ttu-id="2de22-114">[**CreatePrintControl (IWICImagingFactory \* , IPrintDocumentPackageTarget \* , D2D1 \_ propiedades de CONTROL de impresión \_ \_&, ID2D1PrintControl \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span><span class="sxs-lookup"><span data-stu-id="2de22-114">[**CreatePrintControl (IWICImagingFactory\*, IPrintDocumentPackageTarget\*, D2D1\_PRINT\_CONTROL\_PROPERTIES&, ID2D1PrintControl\*\*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createprintcontrol(iwicimagingfactory_iprintdocumentpackagetarget_constd2d1_print_control_properties__id2d1printcontrol))</span></span>    | <span data-ttu-id="2de22-115">Crea un objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) que convierte los primitivos de [Direct2D](/windows/desktop/direct2d/direct2d-portal) almacenados en [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) en una representación de página fija.</span><span class="sxs-lookup"><span data-stu-id="2de22-115">Creates an [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) object that converts [Direct2D](/windows/desktop/direct2d/direct2d-portal) primitives stored in [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist) into a fixed page representation.</span></span> <span data-ttu-id="2de22-116">A continuación, el subsistema de impresión usa los primitivos.</span><span class="sxs-lookup"><span data-stu-id="2de22-116">The print sub-system then consumes the primitives.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2de22-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de22-117">Requirements</span></span>



| <span data-ttu-id="2de22-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de22-118">Requirement</span></span> | <span data-ttu-id="2de22-119">Value</span><span class="sxs-lookup"><span data-stu-id="2de22-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2de22-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2de22-120">Header</span></span><br/> | <dl> <span data-ttu-id="2de22-121"><dt>D2d1 \_ 1. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de22-121"><dt>D2d1\_1.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de22-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2de22-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de22-123">**ID2D1Device**</span><span class="sxs-lookup"><span data-stu-id="2de22-123">**ID2D1Device**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
</dt> </dl>

<span data-ttu-id="2de22-124">�</span><span class="sxs-lookup"><span data-stu-id="2de22-124">�</span></span>

<span data-ttu-id="2de22-125">�</span><span class="sxs-lookup"><span data-stu-id="2de22-125">�</span></span>

---
title: Constantes PICTYPE (OleCtl. h)
description: Describa el tipo de un objeto de imagen tal y como lo devolvió el tipo IPicture Get \_ , así como para describir el tipo de imagen en el miembro picType de la estructura PICTDESC que se pasa a OleCreatePictureIndirect.
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf8ad8f678e9b6e463ade9f149b2e1d4bab529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695888"
---
# <a name="pictype-constants"></a><span data-ttu-id="78ab9-103">Constantes de PICTYPE</span><span class="sxs-lookup"><span data-stu-id="78ab9-103">PICTYPE Constants</span></span>

<span data-ttu-id="78ab9-104">Describa el tipo de un objeto de imagen tal y como lo devolvió [**IPicture:: get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), así como para describir el tipo de imagen en el miembro **PicType** de la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) que se pasa a [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="78ab9-104">Describe the type of a picture object as returned by [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type), as well as to describe the type of picture in the **picType** member of the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure that is passed to [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>



| <span data-ttu-id="78ab9-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="78ab9-105">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="78ab9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="78ab9-106">Description</span></span>                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <span data-ttu-id="78ab9-107"><dt>**PICTYPE \_ No INICIALIZAdo**</dt> <dt>(-1)</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-107"><dt>**PICTYPE\_UNINITIALIZED**</dt> <dt>(-1)</dt></span></span> </dl> | <span data-ttu-id="78ab9-108">El objeto de imagen no está inicializado actualmente.</span><span class="sxs-lookup"><span data-stu-id="78ab9-108">The picture object is currently uninitialized.</span></span> <span data-ttu-id="78ab9-109">Este valor solo es válido como valor devuelto de [**IPicture:: get \_ Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) y no es válido con la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="78ab9-109">This value is only valid as a return value from [**IPicture::get\_Type**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) and is not valid with the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <span data-ttu-id="78ab9-110"><dt>**PICTYPE \_ NINGUNO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-110"><dt>**PICTYPE\_NONE**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="78ab9-111">Se creará un nuevo objeto de imagen sin un estado inicializado.</span><span class="sxs-lookup"><span data-stu-id="78ab9-111">A new picture object is to be created without an initialized state.</span></span> <span data-ttu-id="78ab9-112">Este valor solo es válido en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) .</span><span class="sxs-lookup"><span data-stu-id="78ab9-112">This value is valid only in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure.</span></span><br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <span data-ttu-id="78ab9-113"><dt>**PICTYPE \_ MAPA de bits**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-113"><dt>**PICTYPE\_BITMAP**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="78ab9-114">El tipo de imagen es un mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="78ab9-114">The picture type is a bitmap.</span></span> <span data-ttu-id="78ab9-115">Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **BMP** de esa estructura contiene los parámetros de inicialización correspondientes.</span><span class="sxs-lookup"><span data-stu-id="78ab9-115">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **bmp** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <span data-ttu-id="78ab9-116"><dt>**PICTYPE \_ METARCHIVO**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-116"><dt>**PICTYPE\_METAFILE**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="78ab9-117">El tipo de imagen es un metarchivo.</span><span class="sxs-lookup"><span data-stu-id="78ab9-117">The picture type is a metafile.</span></span> <span data-ttu-id="78ab9-118">Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **WMF** de esa estructura contiene los parámetros de inicialización correspondientes.</span><span class="sxs-lookup"><span data-stu-id="78ab9-118">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **wmf** field of that structure contains the relevant initialization parameters.</span></span><br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <span data-ttu-id="78ab9-119"><dt>**PICTYPE \_ ICONO**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-119"><dt>**PICTYPE\_ICON**</dt> <dt>3</dt></span></span> </dl>                               | <span data-ttu-id="78ab9-120">El tipo de imagen es un icono.</span><span class="sxs-lookup"><span data-stu-id="78ab9-120">The picture type is an icon.</span></span> <span data-ttu-id="78ab9-121">Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **Icon** de esa estructura contiene los parámetros de inicialización correspondientes.</span><span class="sxs-lookup"><span data-stu-id="78ab9-121">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **icon** field of that structure contains the relevant initialization parameters.</span></span><br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <span data-ttu-id="78ab9-122"><dt>**PICTYPE \_ ENHMETAFILE**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-122"><dt>**PICTYPE\_ENHMETAFILE**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="78ab9-123">El tipo de imagen es un metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="78ab9-123">The picture type is an enhanced metafile.</span></span> <span data-ttu-id="78ab9-124">Cuando este valor se produce en la estructura [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) , significa que el campo **EMF** de esa estructura contiene los parámetros de inicialización correspondientes.</span><span class="sxs-lookup"><span data-stu-id="78ab9-124">When this value occurs in the [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) structure, it means that the **emf** field of that structure contains the relevant initialization parameters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="78ab9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78ab9-125">Requirements</span></span>



| <span data-ttu-id="78ab9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ab9-126">Requirement</span></span> | <span data-ttu-id="78ab9-127">Value</span><span class="sxs-lookup"><span data-stu-id="78ab9-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78ab9-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78ab9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="78ab9-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="78ab9-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="78ab9-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78ab9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="78ab9-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="78ab9-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="78ab9-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="78ab9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="78ab9-133"><dt>OleCtl. h</dt></span><span class="sxs-lookup"><span data-stu-id="78ab9-133"><dt>OleCtl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78ab9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="78ab9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ab9-135">**IPicture:: get ( \_ tipo)**</span><span class="sxs-lookup"><span data-stu-id="78ab9-135">**IPicture::get\_Type**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[<span data-ttu-id="78ab9-136">**OleCreatePictureIndirect**</span><span class="sxs-lookup"><span data-stu-id="78ab9-136">**OleCreatePictureIndirect**</span></span>](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[<span data-ttu-id="78ab9-137">**PICTDESC**</span><span class="sxs-lookup"><span data-stu-id="78ab9-137">**PICTDESC**</span></span>](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 






---
title: Constantes de barra de idioma Miscelánea (Ctfutb. h)
description: Las constantes de la barra de idioma Miscelánea establecen ciertas propiedades de las barras de idioma.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422539"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="71343-103">Constantes de barra de idioma misceláneas</span><span class="sxs-lookup"><span data-stu-id="71343-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="71343-104">Las constantes de la barra de idioma Miscelánea establecen ciertas propiedades de las barras de idioma.</span><span class="sxs-lookup"><span data-stu-id="71343-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="71343-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="71343-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="71343-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="71343-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="71343-107"><dt>**TF \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="71343-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="71343-108">El elemento de la barra de idioma del sistema debe mostrar el icono especificado para el perfil de idioma.</span><span class="sxs-lookup"><span data-stu-id="71343-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="71343-109">Se usa en los métodos [ITfSystemDeviceTypeLangBarItem:: GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) y [ITfSystemDeviceTypeLangBarItem:: SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .</span><span class="sxs-lookup"><span data-stu-id="71343-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="71343-110"><dt>**TF \_ INVALIDMENUITEM**</dt> <dt>(uint) (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="71343-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="71343-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="71343-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="71343-112"><dt>**TF \_ LBI \_ BMPF \_ vertical**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="71343-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="71343-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="71343-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="71343-114"><dt>**TF \_ LBI \_ DESC \_ Maxlen**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="71343-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="71343-115">Longitud, en caracteres WCHAR, del miembro de estructura [TF \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span><span class="sxs-lookup"><span data-stu-id="71343-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="71343-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71343-116">Requirements</span></span>



| <span data-ttu-id="71343-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="71343-117">Requirement</span></span> | <span data-ttu-id="71343-118">Value</span><span class="sxs-lookup"><span data-stu-id="71343-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71343-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71343-119">Minimum supported client</span></span><br/> | <span data-ttu-id="71343-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71343-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="71343-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71343-121">Minimum supported server</span></span><br/> | <span data-ttu-id="71343-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="71343-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71343-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="71343-123">Redistributable</span></span><br/>          | <span data-ttu-id="71343-124">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="71343-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="71343-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71343-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="71343-126"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71343-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71343-127">IDL</span><span class="sxs-lookup"><span data-stu-id="71343-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71343-128"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71343-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71343-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="71343-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71343-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span><span class="sxs-lookup"><span data-stu-id="71343-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="71343-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span><span class="sxs-lookup"><span data-stu-id="71343-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="71343-132">TF \_ LANGBARITEMINFO</span><span class="sxs-lookup"><span data-stu-id="71343-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 






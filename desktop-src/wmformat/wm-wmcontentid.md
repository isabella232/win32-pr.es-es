---
title: WM/WMContentID
description: El atributo WM/WMContentID contiene un GUID que identifica el contenido.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato de Windows Media WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419605"
---
# <a name="wmwmcontentid"></a><span data-ttu-id="b880b-104">WM/WMContentID</span><span class="sxs-lookup"><span data-stu-id="b880b-104">WM/WMContentID</span></span>

<span data-ttu-id="b880b-105">El atributo **WM/WMContentID** contiene un GUID que identifica el contenido.</span><span class="sxs-lookup"><span data-stu-id="b880b-105">The **WM/WMContentID** attribute contains a GUID identifying the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="b880b-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="b880b-106">Global Constant</span></span>

<span data-ttu-id="b880b-107">g \_ wszWMWMContentID</span><span class="sxs-lookup"><span data-stu-id="b880b-107">g\_wszWMWMContentID</span></span>

## <a name="data-type"></a><span data-ttu-id="b880b-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b880b-108">Data Type</span></span>

<span data-ttu-id="b880b-109">**\_GUID de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b880b-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b880b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b880b-110">Remarks</span></span>

<span data-ttu-id="b880b-111">Las tecnologías de Windows Media identifican el contenido mediante tres valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** y **WM/WMContentID**.</span><span class="sxs-lookup"><span data-stu-id="b880b-111">Content is identified by Windows Media technologies by using three values: **WM/WMCollectionGroupID**, **WM/WMCollectionID**, and **WM/WMContentID**.</span></span> <span data-ttu-id="b880b-112">Estos valores identifican el contenido, la colección a la que pertenece y el grupo al que pertenece la colección.</span><span class="sxs-lookup"><span data-stu-id="b880b-112">These values identify the content, the collection to which it belongs, and the group to which the collection belongs.</span></span> <span data-ttu-id="b880b-113">Los tres valores se rellenan con Windows Media Player cuando se recuperan los metadatos para el contenido.</span><span class="sxs-lookup"><span data-stu-id="b880b-113">All three of these values are populated by Windows Media Player when metadata for the content is retrieved.</span></span> <span data-ttu-id="b880b-114">Puede hacer que la aplicación registre estos valores y utilizarlos para identificar el contenido, pero no debe cambiarlos si están presentes.</span><span class="sxs-lookup"><span data-stu-id="b880b-114">You can have your application record these values and use them to identify content, but you should not change them if they are present.</span></span>

## <a name="see-also"></a><span data-ttu-id="b880b-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b880b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b880b-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="b880b-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





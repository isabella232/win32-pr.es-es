---
title: WM/TrackNumber
description: El atributo WM/TrackNumber contiene el número de pista del contenido. Este atributo se basa en 1.
ms.assetid: cd338cd9-a5de-4311-8089-1d5d90570f69
keywords:
- Formato de Windows Media WM/TrackNumber
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55691335faaf835b270013c6499197c0e3f7bee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714274"
---
# <a name="wmtracknumber"></a><span data-ttu-id="5185c-105">WM/TrackNumber</span><span class="sxs-lookup"><span data-stu-id="5185c-105">WM/TrackNumber</span></span>

<span data-ttu-id="5185c-106">El atributo **WM/TrackNumber** contiene el número de pista del contenido.</span><span class="sxs-lookup"><span data-stu-id="5185c-106">The **WM/TrackNumber** attribute contains the track number of the content.</span></span> <span data-ttu-id="5185c-107">Este atributo se basa en 1.</span><span class="sxs-lookup"><span data-stu-id="5185c-107">This attribute is 1-based.</span></span>

## <a name="global-constant"></a><span data-ttu-id="5185c-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="5185c-108">Global Constant</span></span>

<span data-ttu-id="5185c-109">g \_ wszWMTrackNumber</span><span class="sxs-lookup"><span data-stu-id="5185c-109">g\_wszWMTrackNumber</span></span>

## <a name="data-type"></a><span data-ttu-id="5185c-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5185c-110">Data Type</span></span>

<span data-ttu-id="5185c-111">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="5185c-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="5185c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5185c-112">Remarks</span></span>

<span data-ttu-id="5185c-113">Muchas aplicaciones existentes escriben el valor de **WM/TrackNumber** como **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5185c-113">Many existing applications write the value for **WM/TrackNumber** as a **DWORD**.</span></span> <span data-ttu-id="5185c-114">Si crea una aplicación que reproduzca archivos de orígenes desconocidos, debe incluir código para controlar los valores de cadena y **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5185c-114">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="5185c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="5185c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5185c-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="5185c-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





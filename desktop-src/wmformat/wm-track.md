---
title: WM/pista
description: El atributo WM/Track contiene el número de pista del contenido. Este atributo es de base cero y se admite por compatibilidad con versiones anteriores. En su lugar, el nuevo contenido debe usar el atributo WM/TrackNumber.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- Formato de Windows Media de WM/seguimiento
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419293"
---
# <a name="wmtrack"></a><span data-ttu-id="0d5ca-106">WM/pista</span><span class="sxs-lookup"><span data-stu-id="0d5ca-106">WM/Track</span></span>

<span data-ttu-id="0d5ca-107">El atributo **WM/Track** contiene el número de pista del contenido.</span><span class="sxs-lookup"><span data-stu-id="0d5ca-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="0d5ca-108">Este atributo es de base cero y se admite por compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="0d5ca-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="0d5ca-109">En su lugar, el nuevo contenido debe usar el atributo [**WM/TrackNumber**](wm-tracknumber.md) .</span><span class="sxs-lookup"><span data-stu-id="0d5ca-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0d5ca-110">Constante global</span><span class="sxs-lookup"><span data-stu-id="0d5ca-110">Global Constant</span></span>

<span data-ttu-id="0d5ca-111">g \_ wszWMTrack</span><span class="sxs-lookup"><span data-stu-id="0d5ca-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="0d5ca-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0d5ca-112">Data Type</span></span>

<span data-ttu-id="0d5ca-113">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0d5ca-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5ca-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d5ca-114">Remarks</span></span>

<span data-ttu-id="0d5ca-115">Muchas aplicaciones existentes escriben el valor de **WM/Track** como **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="0d5ca-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="0d5ca-116">Si crea una aplicación que reproduzca archivos de orígenes desconocidos, debe incluir código para controlar los valores de cadena y **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0d5ca-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d5ca-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d5ca-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5ca-118">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="0d5ca-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





---
title: ASFLeakyBucketPairs
description: El atributo ASFLeakyBucketPairs es un atributo opcional que describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- ASFLeakyBucketPairs formato de Windows Media
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105695508"
---
# <a name="asfleakybucketpairs"></a><span data-ttu-id="fb3da-104">ASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="fb3da-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="fb3da-105">El atributo **ASFLeakyBucketPairs** es un atributo opcional que describe los requisitos de almacenamiento en búfer para un archivo de velocidad de bits variable.</span><span class="sxs-lookup"><span data-stu-id="fb3da-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="fb3da-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="fb3da-106">Global Constant</span></span>

<span data-ttu-id="fb3da-107">g \_ wszASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="fb3da-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="fb3da-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fb3da-108">Data Type</span></span>

<span data-ttu-id="fb3da-109">**tipo de WMT \_ \_ binario**</span><span class="sxs-lookup"><span data-stu-id="fb3da-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3da-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb3da-110">Remarks</span></span>

<span data-ttu-id="fb3da-111">Este atributo tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="fb3da-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="fb3da-112">Donde *wReserved* debe ser igual a cero y *bucket* es una matriz de estructuras de pares de [**\_ \_ depósitos \_ con fugas de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) .</span><span class="sxs-lookup"><span data-stu-id="fb3da-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="fb3da-113">La matriz debe contener al menos dos entradas, pero puede ser mayor.</span><span class="sxs-lookup"><span data-stu-id="fb3da-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="fb3da-114">El objeto lector utiliza este atributo para determinar la cantidad de contenido que se va a almacenar en búfer antes de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fb3da-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb3da-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb3da-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3da-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="fb3da-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





---
description: Negociar tipos de medios
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Negociar tipos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689672"
---
# <a name="negotiating-media-types"></a><span data-ttu-id="b6d96-103">Negociar tipos de medios</span><span class="sxs-lookup"><span data-stu-id="b6d96-103">Negotiating Media Types</span></span>

<span data-ttu-id="b6d96-104">Cuando el administrador de gráficos de filtro llama al método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , tiene varias opciones para especificar un tipo de medio:</span><span class="sxs-lookup"><span data-stu-id="b6d96-104">When the Filter Graph Manager calls the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, it has several options for specifying a media type:</span></span>

-   <span data-ttu-id="b6d96-105">**Tipo completo:** Si se especifica el tipo de medio completo, el PIN intenta conectarse con ese tipo.</span><span class="sxs-lookup"><span data-stu-id="b6d96-105">**Complete type:** If the media type is fully specified, the pins attempt to connect with that type.</span></span> <span data-ttu-id="b6d96-106">Si no es así, se produce un error en el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="b6d96-106">If they cannot, the connection attempt fails.</span></span>
-   <span data-ttu-id="b6d96-107">**Tipo de medio parcial:** Un tipo de medio es *parcial* si el tipo principal, el subtipo o el tipo de formato es el GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="b6d96-107">**Partial media type:** A media type is *partial* if the major type, subtype, or format type is GUID\_NULL.</span></span> <span data-ttu-id="b6d96-108">El valor null de GUID \_ actúa como un "carácter comodín", que indica que cualquier valor es aceptable.</span><span class="sxs-lookup"><span data-stu-id="b6d96-108">The value GUID\_NULL acts as a "wildcard," indicating that any value is acceptable.</span></span> <span data-ttu-id="b6d96-109">Los pin negocian un tipo que es coherente con el tipo parcial.</span><span class="sxs-lookup"><span data-stu-id="b6d96-109">The pins negotiate a type that is consistent with the partial type.</span></span>
-   <span data-ttu-id="b6d96-110">**Ningún tipo de medio:** Si Filter Graph Manager pasa un puntero **nulo** , los pin pueden aceptar cualquier tipo de medio que sea aceptable para ambos PIN.</span><span class="sxs-lookup"><span data-stu-id="b6d96-110">**No media type:** If the Filter Graph Manager passes a **NULL** pointer, the pins can agree to any media type that is acceptable to both pins.</span></span>

<span data-ttu-id="b6d96-111">Si los PIN se conectan, la conexión siempre tiene un tipo de medio completo.</span><span class="sxs-lookup"><span data-stu-id="b6d96-111">If the pins do connect, the connection always has a complete media type.</span></span> <span data-ttu-id="b6d96-112">El propósito del tipo de medio proporcionado por el administrador de gráficos de filtros es limitar los tipos de conexión posibles.</span><span class="sxs-lookup"><span data-stu-id="b6d96-112">The purpose of the media type given by the Filter Graph Manager is to limit the possible connection types.</span></span>

<span data-ttu-id="b6d96-113">Durante el proceso de negociación, el PIN de salida propone un tipo de medio llamando al método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6d96-113">During the negotiation process, the output pin proposes a media type by calling the input pin's [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="b6d96-114">El PIN de entrada puede aceptar o rechazar el tipo propuesto.</span><span class="sxs-lookup"><span data-stu-id="b6d96-114">The input pin can accept or reject the proposed type.</span></span> <span data-ttu-id="b6d96-115">Este proceso se repite hasta que el PIN de entrada acepta un tipo o el PIN de salida se queda sin tipos y se produce un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="b6d96-115">This process repeats until either the input pin accepts a type, or the output pin runs out of types and the connection fails.</span></span>

<span data-ttu-id="b6d96-116">La forma en que un terminal de salida selecciona los tipos de medios que se deben proponer depende de la implementación.</span><span class="sxs-lookup"><span data-stu-id="b6d96-116">How an output pin selects media types to propose depends on the implementation.</span></span> <span data-ttu-id="b6d96-117">En las clases base de DirectShow, el PIN de salida llama a [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6d96-117">In the DirectShow base classes, the output pin calls [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) on the input pin.</span></span> <span data-ttu-id="b6d96-118">Este método devuelve un enumerador que enumera los tipos de medios preferidos del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="b6d96-118">This method returns an enumerator that enumerates the input pin's preferred media types.</span></span> <span data-ttu-id="b6d96-119">Si no es así, el PIN de salida enumera sus propios tipos preferidos.</span><span class="sxs-lookup"><span data-stu-id="b6d96-119">Failing that, the output pin enumerates its own preferred types.</span></span>

<span data-ttu-id="b6d96-120">**Trabajar con tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="b6d96-120">**Working with Media Types**</span></span>

<span data-ttu-id="b6d96-121">En cualquier función que reciba un parámetro de **\_ \_ tipo de medio am** , valide siempre los valores de **cbFormat** y **formatType** antes de desreferenciar el miembro **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="b6d96-121">In any function that receives an **AM\_MEDIA\_TYPE** parameter, always validate the values of **cbFormat** and **formattype** before dereferencing the **pbFormat** member.</span></span> <span data-ttu-id="b6d96-122">El código siguiente es incorrecto:</span><span class="sxs-lookup"><span data-stu-id="b6d96-122">The following code is incorrect:</span></span>


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



<span data-ttu-id="b6d96-123">El código siguiente es correcto:</span><span class="sxs-lookup"><span data-stu-id="b6d96-123">The following code is correct:</span></span>


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 




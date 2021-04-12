---
title: En
description: El atributo de búsqueda es un atributo de nivel de archivo que especifica si una aplicación puede buscar puntos dentro del contenido.
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- Formato de Windows Media de búsqueda
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358761"
---
# <a name="seekable"></a><span data-ttu-id="aaf14-104">En</span><span class="sxs-lookup"><span data-stu-id="aaf14-104">Seekable</span></span>

<span data-ttu-id="aaf14-105">El atributo de **búsqueda** es un atributo de nivel de archivo que especifica si una aplicación puede buscar puntos dentro del contenido.</span><span class="sxs-lookup"><span data-stu-id="aaf14-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="aaf14-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="aaf14-106">Global Constant</span></span>

<span data-ttu-id="aaf14-107">g \_ wszWMSeekable</span><span class="sxs-lookup"><span data-stu-id="aaf14-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="aaf14-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aaf14-108">Data Type</span></span>

<span data-ttu-id="aaf14-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="aaf14-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="aaf14-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aaf14-110">Remarks</span></span>

<span data-ttu-id="aaf14-111">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="aaf14-111">This is a coded attribute.</span></span>

<span data-ttu-id="aaf14-112">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="aaf14-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="aaf14-113">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="aaf14-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="aaf14-114">El valor de este atributo para un archivo puede variar en función del objeto que exponga la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) o [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) utilizada para recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="aaf14-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="aaf14-115">Esto se debe a que los objetos del lector (tanto sincrónicos como asincrónicos) realizan una comprobación más exhaustiva que el objeto del editor de metadatos, para determinar si se puede buscar en un punto de un archivo.</span><span class="sxs-lookup"><span data-stu-id="aaf14-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="aaf14-116">El valor del atributo de **búsqueda** devuelto por un objeto lector es más preciso.</span><span class="sxs-lookup"><span data-stu-id="aaf14-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="aaf14-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="aaf14-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf14-118">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="aaf14-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





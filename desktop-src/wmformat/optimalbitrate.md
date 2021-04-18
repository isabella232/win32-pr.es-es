---
title: OptimalBitrate
description: El atributo OptimalBitrate contiene la velocidad de bits a la que se reproduce el archivo.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate formato de Windows Media
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704853"
---
# <a name="optimalbitrate"></a><span data-ttu-id="0cbdf-104">OptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="0cbdf-104">OptimalBitrate</span></span>

<span data-ttu-id="0cbdf-105">El atributo **OptimalBitrate** contiene la velocidad de bits a la que se reproduce el archivo.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0cbdf-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="0cbdf-106">Global Constant</span></span>

<span data-ttu-id="0cbdf-107">g \_ wszWMOptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="0cbdf-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="0cbdf-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0cbdf-108">Data Type</span></span>

<span data-ttu-id="0cbdf-109">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0cbdf-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0cbdf-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0cbdf-110">Remarks</span></span>

<span data-ttu-id="0cbdf-111">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-111">This is a coded attribute.</span></span>

<span data-ttu-id="0cbdf-112">En el caso de los archivos que contienen secuencias de velocidad de bits variable (VBR), este valor es la velocidad de bits máxima de las secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="0cbdf-113">En el caso de los archivos sin VBR, este valor es igual que la [**velocidad de bits**](bit-rate.md).</span><span class="sxs-lookup"><span data-stu-id="0cbdf-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="0cbdf-114">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="0cbdf-115">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="0cbdf-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="0cbdf-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cbdf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cbdf-117">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="0cbdf-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





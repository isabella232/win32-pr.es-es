---
title: CurrentBitrate
description: El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate formato de Windows Media
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714301"
---
# <a name="currentbitrate"></a><span data-ttu-id="93884-104">CurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="93884-104">CurrentBitrate</span></span>

<span data-ttu-id="93884-105">El atributo CurrentBitrate contiene la velocidad de bits total actual de las secuencias activas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="93884-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="93884-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="93884-106">Global Constant</span></span>

<span data-ttu-id="93884-107">g \_ wszWMCurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="93884-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="93884-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="93884-108">Data Type</span></span>

<span data-ttu-id="93884-109">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="93884-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="93884-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93884-110">Remarks</span></span>

<span data-ttu-id="93884-111">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="93884-111">This is a coded attribute.</span></span>

<span data-ttu-id="93884-112">El valor recuperado para **CurrentBitrate** es diferente en función del objeto usado.</span><span class="sxs-lookup"><span data-stu-id="93884-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="93884-113">En el objeto lector o lector sincrónico, el valor es la velocidad de bits real en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="93884-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="93884-114">En el objeto editor de metadatos, el valor es la velocidad de bits promedio del archivo.</span><span class="sxs-lookup"><span data-stu-id="93884-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="93884-115">La velocidad de bits real de un archivo es igual a la velocidad de bits de todas las secuencias activas más la sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="93884-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="93884-116">Este es el valor que se muestra, por ejemplo, cuando se reproduce un archivo con la Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="93884-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="93884-117">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="93884-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="93884-118">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="93884-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="93884-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="93884-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93884-120">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="93884-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 





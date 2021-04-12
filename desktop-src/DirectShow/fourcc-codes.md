---
description: Códigos FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Códigos FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152018"
---
# <a name="fourcc-codes"></a><span data-ttu-id="207a4-103">Códigos FOURCC</span><span class="sxs-lookup"><span data-stu-id="207a4-103">FOURCC Codes</span></span>

<span data-ttu-id="207a4-104">Muchos formatos de medios digitales tienen códigos FOURCC asignados.</span><span class="sxs-lookup"><span data-stu-id="207a4-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="207a4-105">Un código FOURCC es un entero de 32 bits sin signo que se crea mediante la concatenación de cuatro caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="207a4-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="207a4-106">Por ejemplo, el código FOURCC del vídeo YUY2 es "YUY2".</span><span class="sxs-lookup"><span data-stu-id="207a4-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="207a4-107">En el caso de los formatos de vídeo comprimidos y los formatos de vídeo no RGB (como YUV), el miembro de **bicompresión** de la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) debe establecerse en el código FourCC.</span><span class="sxs-lookup"><span data-stu-id="207a4-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="207a4-108">Hay varias macros de C/C++ que facilitan la declaración de valores FOURCC en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="207a4-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="207a4-109">Por ejemplo, la macro **MAKEFOURCC** se declara en mmsystem. h y la macro **FCC** se declara en Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="207a4-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="207a4-110">Úselos de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="207a4-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="207a4-111">También puede declarar un código FOURCC directamente como un literal de cadena simplemente invirtiendo el orden de los caracteres.</span><span class="sxs-lookup"><span data-stu-id="207a4-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="207a4-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="207a4-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="207a4-113">Invertir el orden es necesario porque el sistema operativo Microsoft Windows usa una arquitectura little-endian.</span><span class="sxs-lookup"><span data-stu-id="207a4-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="207a4-114">' Y ' = 0x59, ' U ' = 0x55 y ' 2 ' = 2, por lo que ' 2YUY ' es 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="207a4-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="207a4-115">Convertir códigos FOURCC en GUID de subtipo</span><span class="sxs-lookup"><span data-stu-id="207a4-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="207a4-116">Un intervalo de 2 \* 32 GUID está reservado para representar FOURCCs.</span><span class="sxs-lookup"><span data-stu-id="207a4-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="207a4-117">Estos GUID tienen todo el formato, `XXXXXXXX-0000-0010-8000-00AA00389B71` donde `XXXXXXXX` es el código FourCC.</span><span class="sxs-lookup"><span data-stu-id="207a4-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="207a4-118">Por lo tanto, el GUID del subtipo para YUY2 es `32595559-0000-0010-8000-00AA00389B71` .</span><span class="sxs-lookup"><span data-stu-id="207a4-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="207a4-119">Muchos de estos GUID ya están definidos en el archivo de encabezado UUID. h.</span><span class="sxs-lookup"><span data-stu-id="207a4-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="207a4-120">Por ejemplo, el subtipo YUY2 se define como MEDIASUBTYPE \_ YUY2.</span><span class="sxs-lookup"><span data-stu-id="207a4-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="207a4-121">La biblioteca de clases base de DirectShow también proporciona una clase auxiliar, [**FOURCCMap**](fourccmap.md), que se puede usar para convertir códigos FourCC en valores GUID.</span><span class="sxs-lookup"><span data-stu-id="207a4-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="207a4-122">El constructor **FOURCCMap** toma un código FourCC como parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="207a4-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="207a4-123">Después, puede convertir el objeto **FOURCCMap** al GUID correspondiente:</span><span class="sxs-lookup"><span data-stu-id="207a4-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="207a4-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="207a4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="207a4-125">**Subtipos de audio**</span><span class="sxs-lookup"><span data-stu-id="207a4-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="207a4-126">Subtipos de vídeo</span><span class="sxs-lookup"><span data-stu-id="207a4-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="207a4-127">Trabajar con códecs</span><span class="sxs-lookup"><span data-stu-id="207a4-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 




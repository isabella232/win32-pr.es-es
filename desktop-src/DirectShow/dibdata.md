---
description: La estructura DIBDATA contiene información sobre un mapa de bits independiente del dispositivo GDI (DIB).
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Estructura DIBDATA (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680688"
---
# <a name="dibdata-structure"></a><span data-ttu-id="8d74a-103">Estructura DIBDATA</span><span class="sxs-lookup"><span data-stu-id="8d74a-103">DIBDATA structure</span></span>

<span data-ttu-id="8d74a-104">La `DIBDATA` estructura contiene información sobre un mapa de bits independiente del dispositivo GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="8d74a-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d74a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8d74a-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="8d74a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8d74a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8d74a-107">**PaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="8d74a-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8d74a-108">Este miembro debe incrementarse cada vez que cambie la paleta.</span><span class="sxs-lookup"><span data-stu-id="8d74a-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="8d74a-109">**DibSection**</span><span class="sxs-lookup"><span data-stu-id="8d74a-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="8d74a-110">Estructura **DIBSECTION** que contiene información sobre el Dib.</span><span class="sxs-lookup"><span data-stu-id="8d74a-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="8d74a-111">Consulte la documentación de GDI para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8d74a-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="8d74a-112">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="8d74a-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="8d74a-113">Identificador del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8d74a-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="8d74a-114">**hMapping**</span><span class="sxs-lookup"><span data-stu-id="8d74a-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="8d74a-115">Identificador de un objeto de asignación de archivos que se utiliza para compartir la memoria entre GDI y un objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="8d74a-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="8d74a-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="8d74a-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="8d74a-117">Dirección del mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="8d74a-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d74a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d74a-118">Requirements</span></span>



| <span data-ttu-id="8d74a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d74a-119">Requirement</span></span> | <span data-ttu-id="8d74a-120">Value</span><span class="sxs-lookup"><span data-stu-id="8d74a-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d74a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d74a-121">Header</span></span><br/> | <dl> <span data-ttu-id="8d74a-122"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d74a-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 





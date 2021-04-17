---
title: Estructura de _VIDEOINFOHEADER
description: La \_ estructura VIDEOINFOHEADER contiene información sobre un flujo de vídeo e incluye una \_ estructura BITMAPINFOHEADER que define el formato de un fotograma individual.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Estructura _VIDEOINFOHEADER Administrador de dispositivos de Windows Media
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698533"
---
# <a name="_videoinfoheader-structure"></a><span data-ttu-id="175c0-104">\_Estructura VIDEOINFOHEADER</span><span class="sxs-lookup"><span data-stu-id="175c0-104">\_VIDEOINFOHEADER structure</span></span>

<span data-ttu-id="175c0-105">La estructura **\_ VIDEOINFOHEADER** contiene información sobre un flujo de vídeo e incluye una estructura **\_ BITMAPINFOHEADER** que define el formato de un fotograma individual.</span><span class="sxs-lookup"><span data-stu-id="175c0-105">The **\_VIDEOINFOHEADER** structure contains information about a video stream and includes a **\_BITMAPINFOHEADER** structure that defines the format of an individual frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="175c0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="175c0-106">Syntax</span></span>


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="175c0-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="175c0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="175c0-108">**rcSource**</span><span class="sxs-lookup"><span data-stu-id="175c0-108">**rcSource**</span></span>
</dt> <dd>

<span data-ttu-id="175c0-109">Estructura **Rect** que especifica la ventana de vídeo de origen.</span><span class="sxs-lookup"><span data-stu-id="175c0-109">**RECT** structure that specifies the source video window.</span></span>

</dd> <dt>

<span data-ttu-id="175c0-110">**rcTarget**</span><span class="sxs-lookup"><span data-stu-id="175c0-110">**rcTarget**</span></span>
</dt> <dd>

<span data-ttu-id="175c0-111">Estructura **Rect** que especifica la ventana de vídeo de destino.</span><span class="sxs-lookup"><span data-stu-id="175c0-111">**RECT** structure that specifies the destination video window.</span></span>

</dd> <dt>

<span data-ttu-id="175c0-112">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="175c0-112">**dwBitRate**</span></span>
</dt> <dd>

<span data-ttu-id="175c0-113">Valor **DWORD** que especifica la velocidad de datos aproximada del flujo de vídeo, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="175c0-113">**DWORD** value that specifies the video stream's approximate data rate, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="175c0-114">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="175c0-114">**dwBitErrorRate**</span></span>
</dt> <dd>

<span data-ttu-id="175c0-115">Valor **DWORD** que especifica la tasa de errores de datos de la secuencia de vídeo, en errores de bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="175c0-115">**DWORD** value that specifies the video stream's data error rate, in bit errors per second.</span></span>

</dd> <dt>

<span data-ttu-id="175c0-116">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="175c0-116">**AvgTimePerFrame**</span></span>
</dt> <dd>

<span data-ttu-id="175c0-117">**Referencia \_ de** Valor de tiempo que especifica el promedio de tiempo de visualización del fotograma de vídeo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="175c0-117">**REFERENCE\_TIME** value that specifies the video frame's average display time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="175c0-118">**bmiHeader**</span><span class="sxs-lookup"><span data-stu-id="175c0-118">**bmiHeader**</span></span>
</dt> <dd>

<span data-ttu-id="175c0-119">Estructura **\_ BITMAPINFOHEADER** de Win32 que contiene información de color y dimensión para el mapa de bits de imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="175c0-119">Win32 **\_BITMAPINFOHEADER** structure that contains color and dimension information for the video image bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="175c0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="175c0-120">Requirements</span></span>



| <span data-ttu-id="175c0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="175c0-121">Requirement</span></span> | <span data-ttu-id="175c0-122">Value</span><span class="sxs-lookup"><span data-stu-id="175c0-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="175c0-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="175c0-123">Header</span></span><br/> | <dl> <span data-ttu-id="175c0-124"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="175c0-124"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175c0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="175c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175c0-126">**\_BITMAPINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="175c0-126">**\_BITMAPINFOHEADER**</span></span>](-bitmapinfoheader.md)
</dt> <dt>

[<span data-ttu-id="175c0-127">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="175c0-127">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 






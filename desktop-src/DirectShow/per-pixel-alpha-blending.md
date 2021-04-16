---
description: Per-Pixel combinación alfa
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel combinación alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686339"
---
# <a name="per-pixel-alpha-blending"></a>Per-Pixel combinación alfa

Se han definido cuatro subtipos de medios para la combinación alfa por píxel. Estos subtipos solo se admiten cuando el VMR está en modo de mezcla. VMR rechazará la conexión si no está en modo de mezcla cuando un filtro de nivel superior intenta conectarse utilizando uno de estos subtipos. Estos subtipos se definen en UUID. h:

-   MEDIASUBTYPE \_ ARGB1555
-   MEDIASUBTYPE \_ ARGB4444
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ AYUV

Para obtener más información, vea subtipos de [vídeo RGB sin comprimir](uncompressed-rgb-video-subtypes.md) y [**subtipos de vídeo YUV**](yuv-video-subtypes.md).

 

 




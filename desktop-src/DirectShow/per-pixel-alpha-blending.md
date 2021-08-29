---
description: Per-Pixel combinación alfa
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel combinación alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8722c0483ab4308d2f9d91da7ab94435efc666af5b4353970ff0af54af70532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072859"
---
# <a name="per-pixel-alpha-blending"></a>Per-Pixel combinación alfa

Se han definido cuatro subtipos multimedia para la combinación alfa por píxel. Estos subtipos solo se admiten cuando vmr está en modo de combinación. El VMR rechazará la conexión si no está en modo de combinación cuando un filtro ascendente intenta conectarse mediante uno de estos subtipos. Estos subtipos se definen en uuids.h:

-   MEDIASUBTYPE \_ ARGB1555
-   MEDIASUBTYPE \_ ARGB4444
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ AYUV

Para obtener más información, [vea Subtipos](uncompressed-rgb-video-subtypes.md) de vídeo RGB sin comprimir y [**Subtipos de vídeo YUV**](yuv-video-subtypes.md).

 

 




---
description: Acceso a las superficies de DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Acceso a las superficies de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906830"
---
# <a name="access-to-directdraw-surfaces"></a>Acceso a las superficies de DirectDraw

Los objetos de ejemplo multimedia que proporcionan los filtros de la VMR a los de nivel superior admiten la interfaz [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Para obtener la interfaz, llame a QueryInterface en la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) y especifique IID \_ IVMRSurface. Los filtros ascendentes pueden usar los métodos de IVMRSurface para tener acceso y manipular la superficie que ha creado el VMR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la VMR para desarrolladores de filtros de DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 




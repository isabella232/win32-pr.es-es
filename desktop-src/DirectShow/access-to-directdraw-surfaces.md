---
description: Acceso a las superficies de DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Acceso a las superficies de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff443550cb6a922a3361b6d75b880eb427edf79e3a3232c21ab6aad0c06ec483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873575"
---
# <a name="access-to-directdraw-surfaces"></a>Acceso a las superficies de DirectDraw

Los objetos media sample proporcionados por vmr para los filtros ascendentes admiten la [**interfaz IVMRSurface.**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) Para obtener la interfaz, llame a QueryInterface en la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) y especifique IID \_ IVMRSurface. A continuación, los filtros ascendentes pueden usar los métodos IVMRSurface para tener acceso a la superficie creada por vmr y manipularla.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VMR para DirectShow de filtros](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 




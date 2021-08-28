---
description: Filtro Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b51dceb2a7f82a91fe30275cacfaad4ad78eded
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987358"
---
# <a name="overlay-mixer-2-filter"></a>Filtro Mixer 2

El filtro Overlay Mixer 2 es idéntico al filtro [overlay Mixer,](overlay-mixer-filter.md) excepto:

-   Solo admite tipos multimedia con [**formatos VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)
-   Tiene un mayor grado, lo que permite agregarlo automáticamente a un gráfico de filtros.

Se proporciona el Mixer superposición 2 para que el Administrador de filtros Graph lo agregue al gráfico cuando represente vídeo MPEG-2 que no sea DVD. El componente que compila el gráfico controla la elección de si se va a usar el Mixer de superposición o la superposición Mixer 2, ya sea filter Graph Manager, Capture Graph Builder o DVD Graph Builder. Desde la perspectiva de la aplicación, son el mismo filtro, con las mismas interfaces y funcionalidad.

La tabla siguiente contiene información específica de overlay Mixer 2. Para todos los demás datos de filtro, consulte la documentación de overlay Mixer.




| Etiqueta | Value |
|--------|-------|
| Tipos de medios de pin de entrada | Tipo de formato: Format_VIDEOINFO2 | 
| Filtrar CLSID | CLSID_OverlayMixer2 | 
| <a href="merit.md">Mérito</a> | <ul><li>MERIT_UNLIKELY</li><li>Windows Vista o posterior: MERIT_DO_NOT_USE</li></ul> | 




 

En Windows Vista o versiones posteriores, el motivo del filtro Overlay Mixer 2 es QUE NO USE EL ARGUMENTO, ya que los representadores de vídeo más recientes \_ \_ \_ (VMR-7, VMR-9 y EVR) admiten todos los formatos **VIDEOINFOHEADER2** y, por tanto, no es necesario usar el Mixer de superposición.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 




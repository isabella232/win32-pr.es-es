---
description: Requisitos mínimos de DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Requisitos mínimos de DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997919"
---
# <a name="dmo-minimum-requirements"></a>Requisitos mínimos de DMO

Cada DMO debe cumplir los siguientes requisitos mínimos:

-   Debe admitir la agregación.
-   Debe exponer la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .
-   El modelo de subprocesos debe ser ' both '. DMOs debe funcionar correctamente en un entorno de subprocesamiento libre.

El efecto de audio DMOs debe ser compatible con la interfaz [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) para su uso en DirectMusic y DirectSound.

Las siguientes interfaces se documentan en otro lugar, pero son útiles para muchos DMOs. Sin embargo, no son necesarios.

-   **ISpecifyPropertyPages**, **IPropertyPage**: estas interfaces permiten a DMO proporcionar una página de propiedades para que el usuario establezca las propiedades.
-   **IPersistStream**: esta interfaz permite a DMO guardar su estado en un almacenamiento persistente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): estas interfaces permiten a un cliente configurar el formato de salida de un codificador y la configuración de compresión. (Estas dos interfaces forman parte de la API de DirectShow, pero también se recomiendan para DMOs).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de DMO](writing-a-dmo.md)
</dt> </dl>

 

 




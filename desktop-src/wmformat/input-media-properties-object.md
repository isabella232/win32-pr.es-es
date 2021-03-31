---
title: Objeto de propiedades de medios de entrada
description: Objeto de propiedades de medios de entrada
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- SDK de Windows Media Format, objetos de propiedades de medios de entrada
- Advanced Systems Format (ASF), objetos de propiedades de medios de entrada
- ASF (formato de sistemas avanzados), objetos de propiedades de medios de entrada
- objetos, objetos de propiedades de medios de entrada
- objetos de propiedades de medios de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904398"
---
# <a name="input-media-properties-object"></a>Objeto de propiedades de medios de entrada

Un objeto de propiedades de medios de entrada creado por el objeto de escritor admite las interfaces siguientes. Se tiene acceso a estas interfaces mediante una llamada a **QueryInterface** en una de las interfaces del objeto escritor.



| Interfaz                                        | Descripción                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Recupera las propiedades de un flujo de entrada.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Se usa como la interfaz base para las otras interfaces de propiedad de medios (entrada, salida y vídeo).             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Administra las propiedades de una secuencia de vídeo. Se trata de una interfaz opcional, disponible solo para secuencias de vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Objeto de Writer**](writer-object.md)
</dt> </dl>

 

 





---
title: Objeto De propiedades de medios de entrada
description: Objeto De propiedades de medios de entrada
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows SDK de formato multimedia, objetos de propiedades multimedia de entrada
- Formato de sistemas avanzados (ASF), objetos de propiedades de medios de entrada
- ASF (formato de sistemas avanzados), objetos de propiedades de medios de entrada
- objects,input media properties objects
- objetos de propiedades de medios de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466710"
---
# <a name="input-media-properties-object"></a>Objeto De propiedades de medios de entrada

Un objeto de propiedades multimedia de entrada creado por el objeto de escritor admite las interfaces siguientes. Se accede a estas interfaces mediante una llamada a **QueryInterface** en una de las interfaces del objeto de escritor.



| Interfaz                                        | Descripción                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | Recupera las propiedades de un flujo de entrada.                                                               |
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Se usa como interfaz base para las demás interfaces de propiedad multimedia (entrada, salida y vídeo).             |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Administra las propiedades de una secuencia de vídeo. Se trata de una interfaz opcional, disponible solo para secuencias de vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de Writer**](writer-object.md)
</dt> </dl>

 

 





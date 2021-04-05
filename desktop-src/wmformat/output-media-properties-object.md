---
title: Objeto de propiedades de medios de salida
description: Objeto de propiedades de medios de salida
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- SDK de formato de Windows Media, objetos de propiedades de medios de salida
- Advanced Systems Format (ASF), objetos de propiedades de medios de salida
- ASF (formato de sistemas avanzados), objetos de propiedades de medios de salida
- objetos, propiedades de elementos multimedia de salida
- objetos de propiedades de medios de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104077448"
---
# <a name="output-media-properties-object"></a>Objeto de propiedades de medios de salida

Se usa un objeto de propiedades de medios de salida para recuperar y establecer una propiedad de salida. Se crean objetos de las propiedades de los medios de salida para los formatos de salida compatibles de las secuencias en un archivo que se carga en un objeto de lector. En el caso de las secuencias comprimidas, las propiedades de salida se determinan mediante las posibles salidas del códec de descompresión.

[**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) crea un objeto de las propiedades de los medios de salida. este método crea un objeto de propiedades de medios de salida que contiene las propiedades del formato de salida predeterminado. Es posible que se admitan otros formatos para una salida. Para obtener formatos de salida adicionales, puede llamar a [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obtener el número de formatos de salida admitidos y, a continuación, recorra en bucle mediante llamadas a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat** crea un objeto de propiedades de medios de salida rellenado con los datos para el formato de salida seleccionado.

Los objetos de las propiedades de los medios de salida también se pueden crear con el lector sincrónico. Todos los nombres de método son idénticos a los del lector y todos los exponen la interfaz [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

**GetOutputProps** y **GetOutputFormat** establecen un puntero a una interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) . Las demás interfaces del objeto de propiedades de los medios de salida se pueden obtener llamando al método **QueryInterface** .

Cada objeto de propiedades de medios de salida admite las siguientes interfaces.



| Interfaz                                          | Descripción                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Se usa como la interfaz base para las otras interfaces de propiedad de medios (entrada, salida y vídeo).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Recupera las propiedades de una salida.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Administra las propiedades de una secuencia de vídeo. Se trata de una interfaz opcional, disponible solo para secuencias de vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> </dl>

 

 





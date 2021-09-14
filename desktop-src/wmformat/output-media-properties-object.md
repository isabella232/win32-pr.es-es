---
title: Objeto de propiedades de medios de salida
description: Objeto de propiedades de medios de salida
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows SDK de formato multimedia, objetos de propiedades de medios de salida
- Formato de sistemas avanzados (ASF), objetos de propiedades de medios de salida
- ASF (formato de sistemas avanzados), objetos de propiedades de medios de salida
- objects,output media properties objects
- objetos de propiedades de medios de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266964"
---
# <a name="output-media-properties-object"></a>Objeto de propiedades de medios de salida

Un objeto de propiedades de medios de salida se usa para recuperar y establecer una propiedad de salida. Los objetos de propiedades de medios de salida se crean para los formatos de salida admitidos de secuencias en un archivo que se carga en un objeto de lector. En el caso de los flujos comprimidos, las propiedades de salida están determinadas por las posibles salidas del códec de descompresión.

[**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) Crea un objeto de propiedades de medios de salida. Este método crea un objeto de propiedades de medios de salida que contiene las propiedades del formato de salida predeterminado. Es posible que se admiten otros formatos para una salida. Para obtener formatos de salida adicionales, puede llamar a [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obtener el número de formatos de salida admitidos y, a continuación, recorrerlos en bucle mediante llamadas a [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat crea** un objeto de propiedades de medios de salida rellenado con los datos para el formato de salida seleccionado.

Los objetos de propiedades de medios de salida también se pueden crear con el lector sincrónico. Todos los nombres de método son idénticos a los del lector y todos se exponen mediante la [**interfaz IWMSyncReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)

**GetOutputProps** y **GetOutputFormat** establecen un puntero a una [**interfaz IWMOutputMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) Las demás interfaces del objeto de propiedades de medios de salida se pueden obtener llamando al **método QueryInterface.**

Todas las propiedades de medios de salida admiten las interfaces siguientes.



| Interfaz                                          | Descripción                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Se usa como interfaz base para las demás interfaces de propiedad multimedia (entrada, salida y vídeo).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Recupera las propiedades de una salida.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Administra las propiedades de una secuencia de vídeo. Se trata de una interfaz opcional, disponible solo para secuencias de vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> </dl>

 

 





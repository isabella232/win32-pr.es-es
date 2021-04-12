---
title: Proporcionar una interfaz de usuario
description: Proporcionar una interfaz de usuario
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Complementos de Windows Media Player, páginas de propiedades
- complementos, páginas de propiedades
- Complementos de procesamiento de señal digital, páginas de propiedades
- Complementos DSP, páginas de propiedades
- Complementos de procesamiento de señal digital, interfaz de usuario
- Complementos DSP, interfaz de usuario
- páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269183"
---
# <a name="providing-a-user-interface"></a>Proporcionar una interfaz de usuario

Los complementos DSP pueden proporcionar una página de propiedades para crear una interfaz de usuario. Para ello, el complemento debe incluir un objeto de página de propiedades que proporcione una implementación de una interfaz **IPropertyPage** . El objeto de complemento DSP debe implementar **ISpecifyPropertyPages:: GetPages**, que permite a Windows Media Player buscar e identificar la página de propiedades correcta para el complemento.

**Mostrar un gráfico de estado**

Los complementos de DSP pueden mostrar un gráfico pequeño, o una serie de gráficos, en el área de estado de Windows Media Player para notificar al usuario que hay un complemento activo. Para admitir esta característica, el complemento debe implementar la interfaz **IPropertyBag** . Windows Media Player llama a **IPropertyBag:: Read**, proporcionando un puntero al nombre de propiedad solicitado "IconStreams", que distingue entre mayúsculas y minúsculas, y un puntero a una estructura **Variant** que recibe los datos para el gráfico. El complemento crea un objeto **IStream** (o un SafeArray de objetos **IStream** si hay varios gráficos), después carga los datos gráficos, incluida la información de encabezado, en la secuencia y, a continuación, devuelve un puntero al objeto **IStream** mediante el miembro **punkVal** de la estructura **Variant** . Si el complemento solo proporciona un gráfico, especifica el miembro **VT** de la estructura **variante** como VT \_ desconocido. Si el complemento proporciona varios objetos de **IStream** de gráficos mediante SafeArray, especifica el miembro **VT** de la estructura **Variant** como \_ matriz VT.

Los gráficos pueden almacenarse en diversos formatos de archivo, entre los que se incluyen:

**BMP**

Las imágenes de mapa de bits de Microsoft Windows no están comprimidas.

**JPEG**

Formato de imagen comprimido que se usa habitualmente para las páginas Web. Normalmente, los archivos de formato JPEG tienen extensiones de nombre de archivo. jpg.

**GIF**

Formato de imagen comprimido que se usa habitualmente para las páginas Web.

**PNG**

Formato de imagen comprimido que se usa habitualmente para las páginas Web.

Las dimensiones máximas de los gráficos de complementos de DSP son de 38 píxeles de ancho y de 14 píxeles de alto.

La secuencia de bytes **IStream** que contiene el gráfico de Estado debe incluir información de encabezado. Sin información de encabezado, Windows Media Player no puede identificar correctamente el tipo de gráfico y, por lo tanto, no cargará la imagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 





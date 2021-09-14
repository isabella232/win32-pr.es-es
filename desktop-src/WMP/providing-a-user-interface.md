---
title: Proporcionar un Interfaz de usuario
description: Proporcionar un Interfaz de usuario
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Reproductor de Windows Media complementos,páginas de propiedades
- complementos, páginas de propiedades
- complementos de procesamiento de señales digitales, páginas de propiedades
- Complementos de DSP, páginas de propiedades
- complementos de procesamiento de señales digitales, interfaz de usuario
- Complementos de DSP, interfaz de usuario
- páginas de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073237"
---
# <a name="providing-a-user-interface"></a>Proporcionar un Interfaz de usuario

Los complementos de DSP pueden proporcionar una página de propiedades para crear una interfaz de usuario. Para ello, el complemento debe incluir un objeto de página de propiedades que proporciona una implementación de una **interfaz IPropertyPage.** El objeto de complemento DSP debe implementar **ISpecifyPropertyPages::GetPages**, lo que permite a Reproductor de Windows Media buscar e identificar la página de propiedades correcta para el complemento.

**Mostrar un gráfico de estado**

Los complementos de DSP pueden mostrar un gráfico pequeño, o serie de gráficos, en el área de estado Reproductor de Windows Media para notificar al usuario que un complemento está activo. Para admitir esta característica, el complemento debe implementar la **interfaz IPropertyBag.** Reproductor de Windows Media llama a **IPropertyBag::Read**, proporcionando un puntero al nombre de propiedad solicitado "IconStreams", que distingue mayúsculas de minúsculas, y un puntero a una estructura **VARIANT** que recibe los datos del gráfico. El complemento crea un objeto **IStream** (o SAFEARRAY de objetos **IStream** si hay varios gráficos), carga los datos gráficos, incluida la información de encabezado, en la secuencia y, a continuación, devuelve un puntero al objeto **IStream** mediante el **miembro recordsetVal** de la **estructura VARIANT.** Si el complemento solo proporciona un gráfico, especifica el miembro **vt** de la **estructura VARIANT** como VT \_ UNKNOWN. Si el complemento proporciona varios objetos **IStream** gráficos mediante SAFEARRAY, especifica el miembro **vt** de la **estructura VARIANT** como VT \_ ARRAY.

Los gráficos se pueden almacenar en una variedad de formatos de archivo, incluidos:

**BMP**

Las imágenes Windows bitmap de Microsoft están descomprimidas.

**JPEG**

Formato de imagen comprimido que se usa normalmente para las páginas web. Normalmente, los archivos de formato JPEG .jpg extensiones de nombre de archivo.

**GIF**

Formato de imagen comprimido que se usa normalmente para las páginas web.

**PNG**

Formato de imagen comprimido que se usa normalmente para las páginas web.

Las dimensiones máximas de los gráficos del complemento DSP son de 38 píxeles de ancho y 14 píxeles de alto.

La secuencia de bytes **IStream** que contiene el gráfico de estado debe incluir información de encabezado. Sin información de encabezado, Reproductor de Windows Media puede identificar correctamente el tipo de gráfico y, por tanto, no cargará la imagen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 





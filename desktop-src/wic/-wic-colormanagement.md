---
description: El componente de creación de imágenes de Windows (WIC) simplifica la administración del color proporcionando la interfaz IWICColorContext y la interfaz IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Introducción a la administración del color
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1552375ee896173ba8d1fdbf4a9ae19c2af6e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707135"
---
# <a name="color-management-overview"></a>Introducción a la administración del color

Las imágenes digitales proceden de y están destinadas a una variedad de dispositivos, cada uno de los cuales tiene su propia gama y rango dinámico. Si un fotógrafo ha capturado la misma escena en dos cámaras diferentes, los colores de las imágenes resultantes no aparecerán exactamente igual, incluso cuando se representen en el mismo dispositivo de salida, ya que las capacidades de la gama de colores de los dos dispositivos de origen eran diferentes. Del mismo modo, la misma imagen representada en dos dispositivos de destino diferentes aparecerá de forma diferente porque los dispositivos de destino tienen perfiles de color diferentes. Para garantizar una reproducción de color coherente en todos los dispositivos, es necesario crear una asignación desde el perfil de color del dispositivo de origen hasta el perfil de color del dispositivo de destino. La administración del color pretende generar una coincidencia visual cercana y coherente, y es una característica fundamental en la creación de imágenes profesionales.

Poder reproducir de forma coherente el color en escáneres, monitores, impresoras y aplicaciones suena como un objetivo sencillo, pero sin un sistema de administración del color en el sistema operativo, es difícil de lograr. Si cada aplicación necesita generar sus propios perfiles de color, es casi imposible conseguir un intercambio de color coherente en todo el proceso de publicación, lo que incluye el análisis, la edición y la composición, la prueba y la distribución.

El componente de creación de imágenes de Windows (WIC) simplifica la administración del color proporcionando la interfaz [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) y la interfaz [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) . Puede obtener un objeto [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) mediante [**IWICFactory:: CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer). [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) es una abstracción del perfil de color del dispositivo. **IWICColorContext** se inicializa con un marco de mapa de bits, el perfil de color del dispositivo de origen y el perfil de color del dispositivo de destino. Realiza la conversión del marco de mapa de bits.

 

 




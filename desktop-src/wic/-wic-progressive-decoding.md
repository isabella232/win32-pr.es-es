---
description: En este tema se presenta la descodificación progresiva y cómo usar la descodificación progresiva en las aplicaciones.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Información general sobre descodificación progresiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf005dfb5b4cf5a69ca45020776fee9f0641eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278182"
---
# <a name="progressive-decoding-overview"></a>Información general sobre descodificación progresiva

En este tema se presenta la descodificación progresiva y cómo usar la descodificación progresiva en las aplicaciones. También proporciona instrucciones para crear códecs que admiten la descodificación progresiva.

En este tema se incluyen las siguientes secciones.

-   [Introducción](#introduction)
-   [¿Qué es la descodificación progresiva?](#what-is-progressive-decoding)
-   [Compatibilidad con la descodificación progresiva en Windows 7](#progressive-decoding-support-in-windows-7)
-   [Descodificación progresiva de JPEG](#jpeg-progressive-decoding)
-   [Descodificación progresiva de PNG/GIF](#pnggif-progressive-decoding)
    -   [Descodificación progresiva de PNG](#png-progressive-decoding)
    -   [Descodificación progresiva de GIF](#gif-progressive-decoding)
-   [Descodificación progresiva en aplicaciones](#progressive-decoding-in-applications)
-   [Compatibilidad con códecs personalizados para descodificación progresiva](#custom-codec-support-for-progressive-decoding)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

La descodificación progresiva proporciona la capacidad de descodificar y representar gradualmente partes de una imagen antes de que toda la imagen termine de descargarse. Esta característica mejora en gran medida la experiencia del usuario al ver imágenes desde Internet, ya que el usuario no tiene que esperar a que se descargue toda la imagen antes de que pueda comenzar la descodificación. Los usuarios pueden ver una vista previa de la imagen con los datos disponibles durante mucho antes de descargar la imagen completa. Esta característica es esencial para cualquier aplicación que se use para ver imágenes de Internet o de orígenes de datos con ancho de banda limitado.

Windows Imaging Component (WIC) en Windows 7 admite la descodificación progresiva de formatos de imagen populares, como JPEG, PNG y GIF. WIC también admite cualquier códec que no sea de Microsoft habilitado para WIC que implemente la descodificación progresiva. No se admite la codificación progresiva en la versión actual de WIC. En este tema se describe la descodificación progresiva en Windows 7 y el procedimiento para habilitar la descodificación progresiva en las aplicaciones.

## <a name="what-is-progressive-decoding"></a>¿Qué es la descodificación progresiva?

La descodificación progresiva es la capacidad de descodificar gradualmente partes de una imagen de un archivo de imagen incompleto. La descodificación tradicional requiere un archivo de imagen completo antes de que pueda comenzar la descodificación. La descodificación progresiva se inicia después de que haya finalizado la descarga de un nivel progresivo de una imagen. El descodificador realiza un paso de descodificación en el nivel de progresiva actual de la imagen. A continuación, realiza varios pasos de descodificación en la imagen a medida que se descargan todos los niveles progresivas. Cada paso de descodificación revela más de la imagen hasta que la imagen se descarga y descodifica por completo. El número de pasos necesarios para descodificar una imagen completa depende del formato de archivo de imagen y el proceso de codificación que se usa para crear la imagen.

Las imágenes se deben codificar específicamente para implementar la descodificación progresiva, pero no todos los formatos de imagen lo admiten. En la lista siguiente se resumen los requisitos para usar la descodificación progresiva.

-   El archivo de imagen debe admitir la descodificación progresiva. La mayoría de los formatos de imagen no admiten la descodificación progresiva, aunque los formatos de imagen más conocidos son JPEG, PNG y GIF.
-   El archivo de imagen se debe codificar como una imagen progresiva. Los archivos de imagen que no se crearon con la codificación de imagen progresiva no pueden implementar la descodificación progresiva, incluso si el formato de archivo lo admitiría de otra manera.
-   Un códec que admita la descodificación progresiva debe estar disponible. Si un códec no admite la descodificación progresiva, una imagen codificada como imagen progresiva se descodificará como una imagen tradicional.

## <a name="progressive-decoding-support-in-windows-7"></a>Compatibilidad con la descodificación progresiva en Windows 7

Windows 7 proporciona códecs integrados que admiten la descodificación progresiva para formatos de imagen JPEG, PNG y GIF. Cada uno de estos códecs de Windows 7 realiza varias fases de descodificación en una imagen. Cada paso corresponde a un nivel determinado y a la parte de la imagen que se descodifica, lo que conduce a una imagen completamente descodificada.

Cada formato de imagen controla la descodificación progresiva de otra manera. En la tabla siguiente se proporciona información sobre el número de niveles progresivos y el método de descodificación que admiten los formatos de descodificación progresiva de Windows 7. 

| Formato de imágenes | Número de niveles progresivos admitidos | Método de descodificación progresiva |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definido por la imagen                       | Aumentar la resolución       |
| PNG          | 7                                      | Entrelaza                 |
| GIF          | 4                                      | Entrelaza                 |



 

Además, la descodificación progresiva se puede implementar en códecs proporcionando compatibilidad para interfaces y métodos progresivos. Si no se admite la descodificación progresiva en un códec, se deben devolver mensajes de error adecuados si se llama a estos métodos.

## <a name="jpeg-progressive-decoding"></a>Descodificación progresiva de JPEG

La descodificación progresiva de JPEG presenta datos de imagen con una resolución cada vez mayor para cada nivel, hasta que la imagen de resolución completa esté disponible. Cada nivel de la imagen se establece para proporcionar un nivel de resolución diferente. A medida que haya más niveles progresivos disponibles, la imagen se muestra en resoluciones más altas, hasta que se resuelva la imagen de resolución completa.

El número de niveles disponibles y la resolución establecida en cada nivel dependen completamente del formato JPEG codificado. En las dos imágenes siguientes se muestra un ejemplo de descodificación progresiva de JPEG en dos niveles progresivos.

![ejemplos de descodificación progresiva de JPEG](graphics/Progressive_JPEG_Comparison.jpg)

La imagen de la izquierda se descodifica en el nivel 0 progresivo. La imagen de la derecha se descodifica por completo después de cinco niveles progresivos.

## <a name="pnggif-progressive-decoding"></a>Descodificación progresiva de PNG/GIF

La descodificación progresiva de PNG y GIF usa un método de descodificación progresiva entrelazada. El proceso de descodificación para ambos formatos es muy similar.

### <a name="png-progressive-decoding"></a>Descodificación progresiva de PNG

Los archivos de imagen PNG proporcionan siete niveles progresivos para la descodificación, tal como se describe en la especificación PNG. La descodificación progresiva de PNG se implementa descodificando un patrón de píxeles especificado en cada paso del descodificador. El patrón de la siguiente tabla de la especificación PNG se replica en toda la imagen. Cada número representa el nivel progresivo en el que se descodificará el píxel correspondiente.



|     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

En la tabla anterior, puede determinar los píxeles que se descodificarán con cada paso del descodificador. A diferencia del códec GIF de Windows 7, el códec PNG de Windows 7 replica el píxel disponible más a la izquierda en una línea de exploración para rellenar los píxeles vacíos.

En las imágenes siguientes se muestra un ejemplo del códec de descodificación progresiva de PNG de Windows 7 en tres niveles progresivos.

![ejemplos de descodificación progresiva de PNG](graphics/PNG_Progressive_Comparison.jpg)

La imagen en la parte superior izquierda muestra una imagen PNG descodificada en el nivel 0 progresiva. En la imagen superior derecha se muestra la misma imagen PNG descodificada en el nivel 3 progresiva. La imagen inferior muestra la misma imagen completamente descodificada después de 7 niveles progresivos.

### <a name="gif-progressive-decoding"></a>Descodificación progresiva de GIF

Los archivos de imagen GIF proporcionan cuatro niveles progresivos para la descodificación, como se describe en la especificación de GIF. Cada paso rellena determinadas filas dentro de una imagen, lo que produce una imagen completa después del cuarto paso. La siguiente tabla de la especificación GIF muestra las líneas de examen descodificadas por cada paso del descodificador. 

| Número de nivel/número de paso | Líneas de recorrido rellenadas   | Inicio de línea de examen |
|---------------------------|------------------------|--------------------|
| 1                         | Cada octavo línea de exploración | 0                  |
| 2                         | Cada octavo línea de exploración | 4                  |
| 3                         | Cada cuarta línea de exploración | 2                  |
| 4                         | Cada segunda línea de exploración | 1                  |



 

Aunque los códecs pueden especificar el contenido de los píxeles vacíos en un nivel determinado, el códec de Windows GIF rellena las líneas de análisis vacías mediante la replicación de líneas de examen rellenadas por encima de la línea de exploración vacía.

## <a name="progressive-decoding-in-applications"></a>Descodificación progresiva en aplicaciones

La interfaz de descodificación progresiva principal es la interfaz [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) . Para obtener una referencia a la interfaz, consulte un fotograma de imagen ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) para **IWICProgressiveLevelControl**. A continuación, se puede tener acceso a los métodos progresivos desde la interfaz.

El código siguiente proporciona un ejemplo para usar la descodificación progresiva en las aplicaciones.


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



El código anterior proporciona la funcionalidad básica necesaria para implementar la descodificación progresiva en la mayoría de las aplicaciones. Con el código, se puede tener acceso a los niveles progresivos a medida que los datos de píxeles de imagen estén disponibles. La función [**SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) bloquea la ejecución hasta que el nivel que se solicita está disponible.

## <a name="custom-codec-support-for-progressive-decoding"></a>Compatibilidad con códecs personalizados para descodificación progresiva

Los desarrolladores de códecs pueden optar por implementar [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) si sus formatos de imagen admiten la descodificación progresiva. La compatibilidad con la descodificación progresiva no es un requisito para la detección y el arbitraje de WIC. Sin embargo, la descodificación progresiva mejora en gran medida la experiencia del usuario y se debe tener en cuenta la implementación si es posible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Compresión y codificación digitales de Continuous-Tone imágenes fijas: requisitos e instrucciones](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[Formato de intercambio de archivos JPEG](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[Especificación de GIF89a](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Especificación y extensiones de Portable Network Graphics (PNG)](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 




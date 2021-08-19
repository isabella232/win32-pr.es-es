---
description: En este tema se presenta la decodificación progresiva y cómo usar la decodación progresiva en las aplicaciones.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Información general sobre la decodación progresiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a409a337ecd3852a50cb5ca1a410ebd32c7f3226c79aacca20b10733e214fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710053"
---
# <a name="progressive-decoding-overview"></a>Información general sobre la decodación progresiva

En este tema se presenta la decodificación progresiva y cómo usar la decodación progresiva en las aplicaciones. También proporciona directrices para crear códecs que admiten lacodación progresiva.

En este tema se incluyen las siguientes secciones.

-   [Introducción](#introduction)
-   [¿Qué es la decodación progresiva?](#what-is-progressive-decoding)
-   [Compatibilidad con la decodificación progresiva en Windows 7](#progressive-decoding-support-in-windows-7)
-   [Codificación progresiva jpeg](#jpeg-progressive-decoding)
-   [Decodación progresiva de PNG/GIF](#pnggif-progressive-decoding)
    -   [Decodación progresiva de PNG](#png-progressive-decoding)
    -   [Decodación progresiva de GIF](#gif-progressive-decoding)
-   [Decoding progresiva en aplicaciones](#progressive-decoding-in-applications)
-   [Compatibilidad con códecs personalizados para lacodización progresiva](#custom-codec-support-for-progressive-decoding)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

La descodificación progresiva proporciona la capacidad de descodificar y representar incrementalmente partes de una imagen antes de que toda la imagen haya terminado de descargarse. Esta característica mejora considerablemente la experiencia del usuario al ver imágenes desde Internet, ya que el usuario no tiene que esperar a que toda la imagen se descargue antes de que pueda comenzar la decodación. Los usuarios pueden ver una vista previa de la imagen con los datos disponibles mucho antes de que se descargue toda la imagen. Esta característica es esencial para cualquier aplicación que se usa para ver imágenes desde Internet o desde orígenes de datos con ancho de banda limitado.

El Windows Imaging Component (WIC) de Windows 7 admite la codificación progresiva de formatos de imagen populares como JPEG, PNG y GIF. WIC también admite cualquier códec que no sea de Microsoft habilitado para WIC que implemente la decodificación progresiva. La codificación progresiva no se admite en la versión actual de WIC. En este tema se describe la decodación progresiva en Windows 7 y el procedimiento para habilitar la decodación progresiva en las aplicaciones.

## <a name="what-is-progressive-decoding"></a>¿Qué es la decodación progresiva?

La descodificación progresiva es la capacidad de descodificar incrementalmente partes de una imagen a partir de un archivo de imagen incompleto. La decodificación tradicional requiere un archivo de imagen completo antes de que pueda comenzar lacoding. La descodación progresiva se inicia una vez finalizado el proceso de descarga de un nivel progresiva de una imagen. El descodificador realiza un paso de descodificación en el nivel progresiva actual de la imagen. A continuación, realiza varias pasadas de decodificación en la imagen a medida que se descarga cada nivel progresiva. Cada paso de descodificación revela más de la imagen hasta que la imagen se descarga y descodifica por completo. El número de pases necesarios para descodificar una imagen completa depende del formato del archivo de imagen y del proceso de codificación utilizado para crear la imagen.

Las imágenes deben codificarse específicamente para implementar la descodificación progresiva, pero no todos los formatos de imagen lo admiten. En la lista siguiente se resumen los requisitos para usar la decodificación progresiva.

-   El archivo de imagen debe admitir la decodificación progresiva. La mayoría de los formatos de imagen no admiten la codificación progresiva, aunque los formatos de imagen más populares son JPEG, PNG y GIF.
-   El archivo de imagen debe codificarse como una imagen progresiva. Los archivos de imagen que no se crearon con la codificación de imagen progresiva no pueden implementar la codificación progresiva, incluso cuando el formato de archivo lo admitiría de otro modo.
-   Debe estar disponible un códec que admita la decodificación progresiva. Si un códec no admite la descodificación progresiva, una imagen codificada como una imagen progresiva se descodificará como una imagen tradicional.

## <a name="progressive-decoding-support-in-windows-7"></a>Compatibilidad con la decodificación progresiva en Windows 7

Windows 7 proporciona códecs integrados que admiten la codificación progresiva para formatos de imagen JPEG, PNG y GIF. Cada uno de estos Windows 7 códecs realizan varias pasadas de decodificación en una imagen. Cada paso corresponde a un nivel y una parte determinados de la imagen que se descodifica, lo que finalmente conduce a una imagen totalmente descodificada.

Cada formato de imagen controla la decodificación progresiva de una manera diferente. En la tabla siguiente se proporciona información sobre el número de niveles progresivas y el método de decodación admitido por los Windows 7 formatos de decodación progresiva. 

| Formato de imágenes | Número de niveles progresivas admitidos | Método decodación progresiva |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definido por imagen                       | Aumento de la resolución       |
| PNG          | 7                                      | Entrelazado                 |
| GIF          | 4                                      | Entrelazado                 |



 

Además, la decodificación progresiva se puede implementar en códecs proporcionando compatibilidad con interfaces y métodos progresivas. Si no se admite la decodificación progresiva en un códec, se deben devolver los mensajes de error adecuados si se llama a estos métodos.

## <a name="jpeg-progressive-decoding"></a>Codificación progresiva jpeg

La codificación progresiva JPEG presenta datos de imagen con resoluciones cada vez más altas para cada nivel, hasta que la imagen de resolución completa esté disponible. Cada nivel de la imagen se establece para proporcionar un nivel de resolución diferente. A medida que estén disponibles niveles más progresivas, la imagen se muestra en resoluciones más altas, hasta que se resuelve la imagen de resolución completa.

El número de niveles disponibles y la resolución establecida en cada nivel dependen completamente del JPEG codificado. En las dos imágenes siguientes se muestra un ejemplo de la codificación progresiva jpeg en dos niveles progresivas.

![ejemplos de la codificación progresiva jpeg](graphics/Progressive_JPEG_Comparison.jpg)

La imagen de la izquierda se descodifica en el nivel progresiva 0. La imagen de la derecha se descodifica completamente después de cinco niveles progresivas.

## <a name="pnggif-progressive-decoding"></a>Decodación progresiva de PNG/GIF

Tanto la decodación progresiva png como la de GIF usan un método decodación progresiva entrelazado. El proceso de descodización para ambos formatos es muy similar.

### <a name="png-progressive-decoding"></a>Decodación progresiva de PNG

Los archivos de imagen PNG proporcionan siete niveles progresivas para la decodificación, como se describe en la especificación PNG. La descodificación progresiva png se implementa mediante la descodificación de un patrón especificado de píxeles en cada paso del descodificador. El patrón de la tabla siguiente de la especificación PNG se replica en toda la imagen. Cada número representa el nivel progresiva en el que se descodificará el píxel correspondiente.



|  &nbsp;  |  &nbsp;   |  &nbsp;   |  &nbsp;   |   &nbsp;  |  &nbsp;   |  &nbsp;   | &nbsp;    |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

En la tabla anterior, puede determinar los píxeles que se descodificarán con cada paso del descodificador. A diferencia Windows códec GIF 7, el códec PNG Windows 7 replica el píxel más a la izquierda disponible en una línea de examen para rellenar píxeles vacíos.

En las imágenes siguientes se muestra un ejemplo del códec de Windows 7 PNG progresiva en tres niveles progresivas.

![ejemplos de lacodación progresiva de png](graphics/PNG_Progressive_Comparison.jpg)

La imagen de la parte superior izquierda muestra una imagen PNG descodificada en el nivel progresiva 0. La imagen de la parte superior derecha muestra la misma imagen PNG descodificada en el nivel 3 progresiva. La imagen inferior muestra la misma imagen totalmente descodificada después de 7 niveles progresivas.

### <a name="gif-progressive-decoding"></a>Decodación progresiva de GIF

Los archivos de imagen GIF proporcionan cuatro niveles progresivas para lacodización, como se describe en la especificación GIF. Cada paso rellena determinadas filas dentro de una imagen, lo que genera una imagen completa después del cuarto paso. En la tabla siguiente de la especificación GIF se muestra qué líneas de examen se descodifican mediante cada paso del descodificador. 

| Número de nivel/número de paso | Examinar líneas rellenadas   | Inicio de la línea de examen |
|---------------------------|------------------------|--------------------|
| 1                         | Cada octavo análisis de línea | 0                  |
| 2                         | Cada octavo análisis de línea | 4                  |
| 3                         | Cada cuarta línea de examen | 2                  |
| 4                         | Línea de examen por segundo | 1                  |



 

Aunque los códecs pueden especificar el contenido de píxeles vacíos en cualquier nivel determinado, el códec GIF de Windows rellena las líneas de examen vacías mediante la replicación de líneas de examen rellenadas por encima de la línea de examen vacía.

## <a name="progressive-decoding-in-applications"></a>Decoding progresiva en aplicaciones

La interfaz de decoding progresiva principal es [**la interfaz IWICProgressiveLevelControl.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) Para obtener una referencia a la interfaz , consulte un marco de imagen ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) para **IWICProgressiveLevelControl**. A continuación, se puede acceder a los métodos progresivas desde la interfaz .

El código siguiente proporciona un ejemplo para usar la codificación progresiva en aplicaciones.


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



El código anterior proporciona la funcionalidad básica necesaria para implementar la codificación progresiva en la mayoría de las aplicaciones. Con el código, se puede acceder a los niveles progresivas a medida que los datos de píxeles de imagen están disponibles. La [**función SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) bloquea la ejecución hasta que el nivel que se solicita está disponible.

## <a name="custom-codec-support-for-progressive-decoding"></a>Compatibilidad con códecs personalizados para lacodización progresiva

Los desarrolladores de códecs pueden optar por implementar [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) si sus formatos de imagen admiten la decodificación progresiva. La compatibilidad con la decodificación progresiva no es un requisito para la detección y el arbitraje de WIC. Sin embargo, la decodificación progresiva mejora en gran medida la experiencia del usuario y la implementación debe tenerse en cuenta si es posible.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Compresión digital y codificación de imágenes Continuous-Tone still: requisitos e instrucciones](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[Formato de intercambio de archivos JPEG](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[Especificación GIF89a](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Especificación y extensiones de gráficos de red portátiles (PNG)](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 




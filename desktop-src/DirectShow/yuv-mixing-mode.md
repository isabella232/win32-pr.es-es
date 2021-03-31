---
description: Modo de mezcla YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modo de mezcla YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912102"
---
# <a name="yuv-mixing-mode"></a>Modo de mezcla YUV

Este tema se aplica a Windows XP Service Pack 2 o posterior.

A partir de Windows XP Service Pack 2, VMR admite un modo de combinación denominado modo de mezcla de YUV. Este modo es muy útil para las aplicaciones de TV o DVD avanzadas. En él, se compensa parte de la potencia del mezclador VMR para mejorar el rendimiento del hardware de gráficos de bajo consumo que usa un diseño de arquitectura de memoria unificada. El modo de mezcla YUV se admite tanto en VMR-7 como en VMR-9.

**Ventajas**

El modo de mezcla YUV tiene varias ventajas relacionadas con el rendimiento de la representación en el modo de combinación RGB original compatible con VMR:

-   Cuando el VMR está en modo de mezcla YUV, todas las operaciones de composición de secuencias de vídeo y desentrelazado se realizan en el espacio de colores YUV. Las superficies YUV suelen requerir del 50% al 60% menos de ancho de banda de memoria que las superficies RGB equivalentes.
-   El desentrelazado y la composición de secuencias se realizan mediante una sola llamada al controlador de gráficos. El controlador puede usar las funcionalidades de múltiples texturas del hardware gráfico, lo que da como resultado un ahorro de ancho de banda de memoria adicional.

Aunque cualquier aplicación de vídeo puede usar el modo de mezcla YUV, está pensado principalmente para dos tipos de aplicaciones de reproducción de vídeo:

1.  Aplicaciones de TV que muestran subtítulos o teletexto.
2.  Las aplicaciones de DVD muestran datos de subimagen de DVD o subtítulos (CC).

**Restricciones**

El valor de VMR exige un número de restricciones cuando se coloca en el modo de mezcla de YUV:

-   Stream 0 (la secuencia conectada a la clavija de entrada 0) puede ser progresiva o entrelazada; todas las demás secuencias deben ser progresivas.
-   GUID \_ null (modo de trama) no permitido para el flujo 0.
-   \_La trama DeinterlacePref no se puede usar como modo de reserva porque esto podría impedir que se creara un dispositivo de desentrelazado. El modo de mezcla YUV requiere un dispositivo de desentrelazado incluso si el vídeo entrante no está entrelazado.
-   No se pueden realizar cambios en el valor alfa plano asociado con cada flujo de entrada de VMR.
-   El usuario no puede modificar el orden Z de las secuencias de vídeo conectadas. El orden Z predeterminado se toma del orden de anclaje.
-   No se admite la creación de claves de color.
-   El PIN de entrada 0 debe recibir la secuencia de vídeo.
-   Las demás clavijas de entrada solo pueden recibir datos de subsecuencia de vídeo, como subimagen de DVD, subtítulos (CC) o teletexto.
-   Las demás clavijas de entrada solo pueden aceptar formatos de alfa YUV por píxel, como AYUV, AI44 y IA44.
-   Ninguno de los pin de entrada de VMR puede aceptar cualquier formato RGB.
-   Las imágenes de mapa de bits proporcionadas por la aplicación ya no se pueden combinar con el vídeo antes de la presentación en pantalla.
-   Los subprocesos individuales no se pueden invertir horizontal o verticalmente con las funciones de "rectángulo de salida" del mezclador de VMR. Se admite el cambio de posición del flujo "normal" y el cambio de tamaño.
-   El color de fondo de combinación (especificado por [**IVMRMixerControl:: SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) todavía se especifica en el espacio de colores RGB, al igual que en el modo de combinación RGB.

**Configuración**

Las aplicaciones deben configurar explícitamente la VMR para aprovechar el modo de mezcla YUV; el modo de combinación RGB original sigue siendo el modo de mezcla predeterminado. Para habilitar el modo de mezcla YUV en VMR-7, llame a [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con la \_ marca MixerPref RenderTargetYUV. Esta llamada debe realizarse antes de que cualquiera de los pin de entrada de VMR esté conectado. Para habilitar el modo de mezcla YUV en VMR-9, llame a [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la \_ marca MixerPref9 RenderTargetYUV.

La única manera de determinar si VMR-7 admite el nuevo modo de mezcla de YUV es intentar establecer la VMR en ese modo. Si la llamada se realiza correctamente, puede volver a poner la VMR en el modo de mezcla de RGB si es necesario. Una vez establecido en el modo de mezcla YUV, el VMR solo se puede volver a cambiar al modo de mezcla de RGB después de que todos los pin de entrada se hayan desconectado.

En el modo de mezcla YUV, puede reducir la carga de la unidad de procesamiento de gráficos (GPU) aplicando las siguientes marcas en el método **SetMixingPrefs** :



| Marca                                                                                 | Descripción                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Cambie a un desentrelazado de Bob.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | Diezmar la imagen por un factor de 2 horizontal y verticalmente. |



 

Puede Agregar o quitar estas marcas mientras se está ejecutando el gráfico de filtros; el cambio se aplica cuando el mezclador VMR compone el siguiente fotograma de vídeo. Las marcas no son mutuamente excluyentes. Esta configuración reduce la calidad de la imagen, por lo que normalmente se aplican solo cuando la calidad del vídeo es menos importante, por ejemplo, si el vídeo se reproduce en una pequeña parte de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar el modo de mezcla de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 





---
description: Modo de combinación de YUV
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: Modo de combinación de YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 957c5345eb80576ad0371558bb60d0b6651221bd98d7830cb968f39c16330fb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290755"
---
# <a name="yuv-mixing-mode"></a>Modo de combinación de YUV

Este tema se aplica a Windows XP Service Pack 2 o posterior.

A partir Windows XP Service Pack 2, vmr admite un modo de combinación denominado modo de combinación YUV. Este modo es más útil para aplicaciones avanzadas de TV o DVD. Comercializa parte de la potencia del mezclador de VMR para mejorar el rendimiento en hardware gráfico de gama baja que usa un diseño de arquitectura de memoria unificada. El modo de combinación YUV se admite en VMR-7 y VMR-9.

**Ventajas**

El modo de combinación YUV tiene varias ventajas relacionadas con el rendimiento de representación con respecto al modo de combinación RGB original compatible con VMR:

-   Cuando vmr está en modo de combinación YUV, todas las operaciones de desenlazado y composición de secuencias de vídeo se realizan en el espacio de colores YUV. Las superficies YUV normalmente requieren entre un 50 % y un 60 % menos de ancho de banda de memoria que las superficies RGB equivalentes.
-   El desenlazado y la composición de secuencias se realizan mediante una sola llamada al controlador de gráficos. El controlador puede usar las funcionalidades de múltiples texto del hardware gráfico, lo que genera un ahorro adicional de ancho de banda de memoria.

Aunque cualquier aplicación de vídeo puede usar el modo de combinación YUV, está pensada principalmente para dos tipos de aplicación de reproducción de vídeo:

1.  Aplicaciones de televisión que muestran subtítulos o texto teletexto.
2.  Las aplicaciones de DVD muestran datos de subaspección de DVD o subtítulos.

**Restricciones**

La VMR aplica una serie de restricciones cuando se coloca en el modo de combinación YUV:

-   La secuencia 0 (la secuencia conectada al pin de entrada 0) puede ser progresiva o entrelazada; todas las demás secuencias deben ser progresivas.
-   Guid \_ NULL (modo de tejido) no se permite para el flujo 0.
-   DeinterlacePref Weave no se puede usar como modo de reserva porque esto podría impedir la creación de un dispositivo \_ de desenlace. El modo de combinación YUV requiere un dispositivo de desinteresación, incluso si el vídeo entrante no está entrelazado.
-   No se puede realizar ningún cambio en el valor alfa plano asociado a cada flujo de entrada de VMR.
-   El usuario no puede modificar el orden Z de las secuencias de vídeo conectadas. El orden Z predeterminado se toma del orden de anclado.
-   No se admite la clave de color.
-   El pin de entrada 0 debe recibir la secuencia de vídeo.
-   Las otras entradas ancladas solo pueden recibir datos de secuencias de vídeo, como subpestaciones de DVD, subtítulos o texto teletexto.
-   Las demás entradas ancladas solo pueden aceptar formatos alfa YUV por píxel, como AYUV, AI44 e IA44.
-   Ninguna de las patillas de entrada de VMR puede aceptar formatos RGB.
-   Las imágenes de mapa de bits proporcionadas por la aplicación ya no se pueden combinar con el vídeo antes de la presentación en la pantalla.
-   Las sub secuencias individuales no se pueden invertir horizontal o verticalmente mediante las funciones de "rectángulo de salida" del mezclador de VMR. Se admite la posición y el redimensionamiento de secuencias "normales".
-   El color de fondo de mezcla (especificado por [**IVMR MixerControl::SetBackgroundClr)**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)todavía se especifica en el espacio de colores RGB, igual que en el modo de combinación RGB.

**Configuración**

Las aplicaciones deben configurar explícitamente vmr para aprovechar el modo de combinación YUV. el modo de combinación RGB original sigue siendo el modo de combinación predeterminado. Para habilitar el modo de combinación YUV en VMR-7, llame a [**IVMRMixerControl::Set MixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) con la marca MixerPref \_ RenderTargetYUV. Esta llamada debe realizarse antes de que se conecte cualquiera de los pines de entrada de VMR. Para habilitar el modo de combinación de YUV en VMR-9, llame a [**IVMR MixerControl9::Set MixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con la marca MixerPref9 \_ RenderTargetYUV.

La única manera de determinar si VMR-7 admite el nuevo modo de combinación YUV es intentar establecer la VMR en ese modo. Si la llamada se realiza correctamente, puede volver a poner vmr en modo de combinación RGB si es necesario. Después de establecerse en el modo de combinación YUV, la VMR solo se puede volver a cambiar al modo de combinación RGB después de que se hayan desconectado todos los pines de entrada.

En el modo de combinación YUV, puede reducir la carga en la unidad de procesamiento de gráficos (GPU) aplicando las marcas siguientes en el **método Set MixingPrefs:**



| Marca                                                                                 | Descripción                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| VMR-7: MixerPref \_ DynamicSwitchToBOBVMR-9: MixerPref9 \_ DynamicSwitchToBOB<br/> | Cambie al desenlace bob.                                     |
| VMR-7: MixerPref \_ DynamicDecimateBy2VMR-9: MixerPref \_ DynamicDecimateBy2<br/>  | Descima la imagen por un factor de 2 horizontal y verticalmente. |



 

Puede agregar o quitar estas marcas mientras se ejecuta el gráfico de filtros. el cambio se aplica cuando el mezclador de VMR compone el siguiente fotograma de vídeo. Las marcas no son mutuamente excluyentes. Esta configuración reduce la calidad de la imagen, por lo que normalmente solo las aplicaría cuando la calidad del vídeo sea menos importante, por ejemplo, si el vídeo se reproduce en una pequeña parte de la interfaz de usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del modo de combinación de VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 





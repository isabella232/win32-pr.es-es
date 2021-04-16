---
description: Los controles gamma permiten cambiar el modo en que el sistema muestra el contenido de la superficie sin afectar al contenido de la propia superficie.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Controles gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484bcf7e8fa5e07a3bf4bb718cd361330560f8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104565859"
---
# <a name="gamma-controls-direct3d-9"></a>Controles gamma (Direct3D 9)

Los controles gamma permiten cambiar el modo en que el sistema muestra el contenido de la superficie sin afectar al contenido de la propia superficie. Considere estos controles como filtros muy simples que Direct3D aplica a los datos cuando salen de una superficie y antes de que se representen en la pantalla.

Los controles gamma son una propiedad de una cadena de intercambio. Los controles gamma permiten cambiar de forma dinámica cómo se asignan los niveles rojo, verde y azul de una superficie a los niveles reales que el sistema muestra. Al establecer los niveles gamma, puede hacer que la pantalla del usuario parpadee en color rojo cuando se toma el carácter del usuario, verde cuando el carácter recoge un nuevo elemento, y así sucesivamente sin copiar nuevas imágenes en el búfer de fotogramas para lograr el efecto. O bien, puede ajustar los niveles de color para aplicar una inclinación de color a las imágenes en el búfer de reserva.

Siempre hay al menos una cadena de intercambio (la cadena de intercambio implícita) para cada dispositivo porque Direct3D 9 tiene una cadena de intercambio como una propiedad del dispositivo. Dado que la rampa de gamma es una propiedad de la cadena de intercambio, la rampa de gamma se puede aplicar cuando la cadena de intercambio está en la ventana. La rampa de gamma surte efecto inmediatamente. No hay ninguna espera para una operación de sincronización vertical.

Los métodos [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) y [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) permiten manipular los niveles de rampa que afectan a los componentes de color rojo, verde y azul de los píxeles de la superficie antes de que se envíen al convertidor digital a analógico (DAC) para su presentación.

## <a name="gamma-ramp-levels"></a>Niveles de rampa de gamma

En Direct3D, el término rampa de gamma describe un conjunto de valores que asignan el nivel de un componente de color determinado: rojo, verde y azul para todos los píxeles del búfer de fotogramas a los nuevos niveles que la DAC recibe para su presentación. La reasignación se realiza por medio de tres tablas de búsqueda, una para cada componente de color.

Aquí se muestra cómo funciona: Direct3D toma un píxel del búfer de fotogramas y evalúa sus componentes de color rojo, verde y azul. Cada componente se representa con un valor comprendido entre 0 y 65535. Direct3D toma el valor original y lo utiliza para indizar una matriz de elementos 256 (la rampa), donde cada elemento contiene un valor que reemplaza al original. Direct3D realiza este proceso de búsqueda y reemplazo para cada componente de color de cada píxel en el búfer de fotogramas, lo que cambia los colores finales de todos los píxeles en pantalla.

Resulta útil visualizar los valores de la rampa mediante el gráfico, tal como se muestra en los dos gráficos siguientes. El gráfico de la izquierda muestra una rampa que no modifica los colores. El gráfico de la derecha muestra una rampa que impone una desviación negativa al componente de color al que se aplica.

![gráficos de los valores de rampa de gamma](images/gammalv.png)

Los elementos de matriz para el gráfico de la izquierda contienen valores idénticos a su índice-0 en el elemento en el índice 0 y 65535 en el índice 255. Este tipo de rampa es el valor predeterminado, ya que no cambia los valores de entrada antes de que se muestren. El gráfico derecho proporciona más variación; su rampa contiene valores que van desde 0 en el primer elemento hasta 32768 en el último elemento, con valores que abarcan uniformemente entre. El efecto es que el componente de color que usa esta rampa aparece silenciado en la pantalla. No está limitado al uso de gráficos lineales; Si la aplicación puede asignar una asignación arbitraria si es necesario. Incluso puede establecer las entradas en ceros para quitar un componente de color completamente de la pantalla.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Establecimiento y recuperación de niveles de rampa de gamma

Los niveles de rampa de gamma son tablas de búsqueda efectivas que usa Direct3D para asignar los componentes de color del búfer de fotogramas a los nuevos niveles que se van a mostrar. Puede establecer y recuperar los niveles de rampa para la superficie principal llamando a los métodos [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) y [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) . **SetGammaRamp** acepta dos parámetros y **GetGammaRamp** acepta un parámetro. En el caso de **SetGammaRamp**, el primer parámetro es D3DSGR \_ Calibrate o D3DSGR \_ sin \_ calibración. El segundo parámetro, pRamp, es un puntero a una estructura [**D3DGAMMARAMP**](d3dgammaramp.md) . La estructura **D3DGAMMARAMP** contiene matrices de palabras de 3 256 elementos, una matriz cada una para contener las rampas gamma rojo, verde y azul. **GetGammaRamp** tiene un parámetro que toma un puntero a un tipo de **D3DGAMMARAMP** que se rellenará con la rampa gamma actual.

Puede incluir el valor de \_ calibración D3DSGR para el primer parámetro de [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) para invocar al del calibrador al establecer nuevos niveles de gamma. La calibración de rampas de gamma incurre en cierta sobrecarga de procesamiento y no se debe utilizar con frecuencia. La configuración de una rampa de gamma calibrada proporciona un valor gamma uniforme y absoluto para el usuario, independientemente del adaptador de pantalla y del monitor.

No todos los sistemas admiten la calibración gamma. Para determinar si se admite la calibración de gamma, llame a [**GetDeviceCaps**](/windows/desktop/api)y examine el miembro Caps2 de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) asociada después de que el método devuelva. Si la marca de capacidad de D3DCAPS2 \_ CANCALIBRATEGAMMA está presente, se admite la calibración de gamma.

Al establecer nuevos niveles de rampa, tenga en cuenta que los niveles establecidos en las matrices solo se usan cuando la aplicación está en modo de pantalla completa y exclusivo. Cada vez que la aplicación cambia al modo normal, los niveles de rampa se reservan y surten efecto de nuevo cuando la aplicación vuelve al modo de pantalla completa.

Si el dispositivo no admite rampas gamma en el modo de presentación actual de la cadena de intercambio (pantalla completa o con ventanas), no se devuelve ningún valor de error. Las aplicaciones pueden comprobar los \_ bits de capacidad de D3DCAPS2 FULLSCREENGAMMA y D3DCAPS2 \_ CANCALIBRATEGAMMA en el miembro Caps2 del tipo D3DCAPS9 para determinar las capacidades del dispositivo y si un del calibrador está instalado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 

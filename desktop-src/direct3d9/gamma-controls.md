---
description: Los controles Gamma permiten cambiar la forma en que el sistema muestra el contenido de la superficie, sin afectar al contenido de la propia superficie.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Controles Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484bcf7e8fa5e07a3bf4bb718cd361330560f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127565972"
---
# <a name="gamma-controls-direct3d-9"></a>Controles Gamma (Direct3D 9)

Los controles Gamma permiten cambiar la forma en que el sistema muestra el contenido de la superficie, sin afectar al contenido de la propia superficie. Piense en estos controles como filtros muy simples que Direct3D aplica a los datos a medida que sale de una superficie y antes de representarse en la pantalla.

Los controles Gamma son una propiedad de una cadena de intercambio. Los controles Gamma hacen posible cambiar dinámicamente la asignación de los niveles rojo, verde y azul de una superficie a los niveles reales que muestra el sistema. Al establecer niveles gamma, puede hacer que la pantalla del usuario parpadee colores (rojo cuando se toma el carácter del usuario, verde cuando el carácter recoge un nuevo elemento, y así sucesivamente) sin copiar nuevas imágenes en el búfer de fotogramas para lograr el efecto. O bien, puede ajustar los niveles de color para aplicar un sesgo de color a las imágenes del búfer de reserva.

Siempre hay al menos una cadena de intercambio (la cadena de intercambio implícita) para cada dispositivo porque Direct3D 9 tiene una cadena de intercambio como propiedad del dispositivo. Dado que la rampa gamma es una propiedad de la cadena de intercambio, la rampa gamma se puede aplicar cuando se abre una ventana de la cadena de intercambio. La rampa gamma entra en vigor inmediatamente. No hay ninguna espera para una operación de sincronización vertical.

Los [**métodos SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) y [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) permiten manipular los niveles de rampa que afectan a los componentes de color rojo, verde y azul de píxeles de la superficie antes de que se envíen al convertidor digital a análogo (DAC) para su presentación.

## <a name="gamma-ramp-levels"></a>Niveles de rampa gamma

En Direct3D, el término gamma ramp describe un conjunto de valores que asignan el nivel de un componente de color determinado (rojo, verde, azul) para todos los píxeles del búfer de fotogramas a nuevos niveles recibidos por la DAC para su presentación. El remapping se realiza mediante tres tablas de consulta, una para cada componente de color.

Así es como funciona: Direct3D toma un píxel del búfer del marco y evalúa sus componentes de color rojo, verde y azul individuales. Cada componente se representa mediante un valor de 0 a 65535. Direct3D toma el valor original y lo usa para indexar una matriz de 256 elementos (la rampa), donde cada elemento contiene un valor que reemplaza al original. Direct3D realiza este proceso de búsqueda y reemplazo para cada componente de color de cada píxel del búfer de fotogramas, cambiando así los colores finales de todos los píxeles de la pantalla.

Resulta útil visualizar los valores de rampa mediante el grafo, como se muestra en los dos gráficos siguientes. El gráfico izquierdo muestra una rampa que no modifica los colores en absoluto. El gráfico derecho muestra una rampa que impone un sesgo negativo al componente de color al que se aplica.

![gráficos de los valores de la rampa gamma](images/gammalv.png)

Los elementos de matriz del gráfico de la izquierda contienen valores idénticos a su índice: 0 en el elemento en el índice 0 y 65535 en el índice 255. Este tipo de rampa es el valor predeterminado, ya que no cambia los valores de entrada antes de que se muestren. El gráfico derecho proporciona más variación; su rampa contiene valores que van desde 0 en el primer elemento hasta 32768 en el último elemento, con valores que oscilan uniformemente entre ellos. El efecto es que el componente de color que usa esta rampa aparece muted en la pantalla. No se limita al uso de gráficos lineales; si la aplicación puede asignar asignaciones arbitrarias si es necesario. Incluso puede establecer las entradas en ceros para quitar completamente un componente de color de la pantalla.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Establecimiento y recuperación de niveles de rampa gamma

Los niveles de rampa gamma son tablas de consulta que Direct3D usa para asignar los componentes de color del búfer de fotogramas a nuevos niveles que se mostrarán. Puede establecer y recuperar niveles de rampa para la superficie principal llamando a los [**métodos SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) [**y GetGammaRamp.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) **SetGammaRamp** acepta dos parámetros y **GetGammaRamp** acepta un parámetro. Para **SetGammaRamp,** el primer parámetro es D3DSGR \_ CALIBRATION o D3DSGR NO \_ \_ CALIBRATION. El segundo parámetro, pRamp, es un puntero a una [**estructura D3DGAMMARAMP.**](d3dgammaramp.md) La **estructura D3DGAMMARAMP** contiene tres matrices de 256 elementos de WORD, una matriz cada una para contener las rampas gamma rojo, verde y azul. **GetGammaRamp tiene** un parámetro que toma un puntero a un tipo **D3DGAMMARAMP** que se rellenará con la rampa gamma actual.

Puede incluir el valor D3DSGR CALIBRAR para el primer parámetro de \_ [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) para invocar el calibrador al establecer nuevos niveles gamma. La calibración de las rampas gamma incurre en cierta sobrecarga de procesamiento y no se debe usar con frecuencia. Establecer una rampa gamma calibrada proporciona un valor gamma coherente y absoluto para el usuario, independientemente del adaptador de pantalla y el monitor.

No todos los sistemas admiten la calibración gamma. Para determinar si se admite la calibración gamma, llame a [**GetDeviceCaps**](/windows/desktop/api)y examine el miembro Caps2 de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) asociada después de que el método vuelva. Si la marca de funcionalidad D3DCAPS2 \_ CANUGBRATEGAMMA está presente, se admite la calibración gamma.

Al establecer nuevos niveles de rampa, tenga en cuenta que los niveles establecidos en las matrices solo se usan cuando la aplicación está en modo exclusivo a pantalla completa. Cada vez que la aplicación cambia al modo normal, los niveles de rampa se reservan, lo que vuelve a surte efecto cuando la aplicación restablece el modo de pantalla completa.

Si el dispositivo no admite rampas gamma en el modo de presentación actual de la cadena de intercambio (pantalla completa o ventana), no se devuelve ningún valor de error. Las aplicaciones pueden comprobar los bits de funcionalidad DE D3DCAPS2 \_ FULLSCREENGAMMA y D3DCAPS2 CAN DEDICABRATEGAMMA en el miembro Caps2 del tipo D3DCAPS9 para determinar las funcionalidades del dispositivo y si está instalado un \_ calibrador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 

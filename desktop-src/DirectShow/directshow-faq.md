---
description: Preguntas más frecuentes sobre DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Preguntas más frecuentes sobre DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537498"
---
# <a name="directshow-faq"></a>Preguntas más frecuentes sobre DirectShow

En este artículo se responden muchas de las preguntas más frecuentes sobre Microsoft DirectShow.

**¿Qué sistemas operativos admite DirectShow?**

DirectShow está disponible en todas las versiones compatibles de Windows.

**¿Cuántos conocimientos de COM necesito programar con DirectShow?**

Para el desarrollo de aplicaciones, debe comprender los aspectos básicos del trabajo con objetos COM: Cómo crear una instancia de ellos, acceder a las interfaces que exponen y administrar los recuentos de referencias en esas interfaces. El desarrollo de filtros requiere más información sobre COM.

**¿Qué formatos admite DirectShow?**

Vea [formatos admitidos en DirectShow](supported-formats-in-directshow.md).

**¿Hay una lista de compatibilidad de hardware (HCL) de DirectShow?**

No. DirectShow usa las capacidades de hardware de Microsoft DirectDraw y Microsoft DirectSound si están disponibles. Cuando no hay ningún hardware especial disponible, DirectShow usa GDI para dibujar el vídeo  y las \* API multimedia WaveOut para reproducir audio.

**¿Qué lenguajes puedo usar para escribir una aplicación de DirectShow?**

DirectShow está diseñado principalmente para el desarrollo en C++. Un pequeño subconjunto de la API de DirectShow se expone a través de Visual Basic 6,0; sin embargo, esta característica está en desuso.

**¿Se puede acceder a DirectShow a través de código administrado?**

Microsoft no tiene planes actuales para implementar una API de DirectShow administrada.

**¿Qué compilador necesito para el desarrollo de DirectShow?**

Cualquier compilador capaz de generar objetos del modelo de objetos componentes (COM) debería funcionar una vez que el entorno del compilador se haya configurado correctamente.

**¿Cómo se relaciona DirectShow con Microsoft DirectX?**

Internamente, DirectShow usa DirectSound y DirectDraw cuando el hardware lo admite. Los filtros de representador de vídeo y mezclador de superposición usan las superficies DirectDraw 3 y DirectDraw 5. El representador de mezcla de vídeo 7 (solo en Windows XP) usa superficies de DirectDraw 7. El representador de vídeo mezclador 9 y el representador de vídeo mejorado usan las API de Microsoft Direct3D más recientes. No es necesario usar las otras API de DirectX para escribir una aplicación de DirectShow, aunque es posible combinarlas.

**¿Cómo se relaciona DirectShow con Microsoft ActiveMovie?**

ActiveMovie era el nombre original de DirectShow. El término ActiveMovie ya no se usa.

**¿Está disponible el código fuente para la utilidad GraphEdit? ¿Se puede redistribuir GraphEdit?**

No, el origen no está disponible y Graphedt.exe no es redistribuible.

**¿Reemplazar DMOs los filtros de DirectShow?**

Microsoft DirectX media Objects (DMOs) se puede usar en una aplicación de DirectShow. En el caso de los codificadores, descodificadores y efectos, se recomienda escribir un DMO en lugar de un filtro DirectShow. (Nota: Si desea utilizar la aceleración de vídeo de DirectX en el descodificador, debe implementarla como filtro). Para otros propósitos, es posible que un filtro DirectShow sea más adecuado. Para obtener más información sobre DMOs, vea [objetos multimedia de DirectX](directx-media-objects.md).

**Voy a reproducir un archivo de formato AVI con Windows Media Player. Puedo oír el audio, pero no parece que ningún vídeo, sino que solo veo negro. ¿Qué pasa?**

Probablemente el archivo se ha codificado con un códec que no está presente en el sistema. Aunque el formato de archivo AVI es común, los archivos AVI se pueden crear con muchos formatos de compresión diferentes (códecs). Si intenta reproducir un archivo AVI que usa un códec no compatible, puede oír el componente de audio, pero el vídeo se mostrará como una pantalla en negro o el contenido de la pantalla permanecerá sin cambios.

> [!Note]  
> Windows Media Player a menudo intenta descargar e instalar un códec si no está presente en el sistema.

 

**¿Cómo compilar mi aplicación? ¿Qué bibliotecas y archivos de encabezado necesito?**

Vea [configurar el entorno de compilación](setting-up-the-build-environment.md).

**GraphEdit muestra muchos filtros que no están documentados. ¿Cuáles son estos filtros?**

GraphEdit enumera todos los filtros que están registrados en el sistema en una categoría de filtro. Esto puede incluir filtros instalados por aplicaciones de terceros o instalados por otras tecnologías de Microsoft, como Windows Media o NetMeeting. Además, algunos filtros de DirectShow actúan como contenedores para códecs o dispositivos de hardware, donde cada códec o dispositivo aparece como un filtro distinto. NetMeeting usa el códec de vídeo Microsoft H. 263 y ya no se admite en DirectShow. Para obtener más información, vea [enumerar dispositivos y filtros](enumerating-devices-and-filters.md).

**Tengo problemas para compilar el gráfico personalizado mediante programación.**

En primer lugar, intente compilar el gráfico de filtro con GraphEdit. Esta herramienta le permite simular muchas posibilidades rápidamente. GraphEdit es siempre un excelente lugar para probar el gráfico antes de intentar compilarlo con el código fuente.

Para obtener más información sobre la creación de gráficos, consulte los siguientes artículos:

-   [Compilar el gráfico de filtro](building-the-filter-graph.md)
-   [Enumerar objetos en un gráfico de filtros](enumerating-objects-in-a-filter-graph.md)

**¿Cómo puedo detectar si DirectShow está instalado en un equipo determinado?**

Llame a **CoCreateInstance** para crear una instancia del administrador de gráficos de filtro. Si la llamada se realiza correctamente, DirectShow se instala en la máquina. El código siguiente muestra cómo hacerlo:


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



**Cómo cambiar la configuración de un filtro sin mostrar la página de propiedades**

La mayoría de los filtros exponen una o más interfaces para establecer las propiedades del filtro. Consulte la página de referencia del filtro en cuestión. (Consulte [filtros de DirectShow](directshow-filters.md)).

**¿Puedo probar el filtro con GraphEdit?**

Mientras desarrolla un filtro, GraphEdit puede ayudarle a visualizar las conexiones entre los filtros. También puede proporcionar una prueba rápida de la funcionalidad de un filtro. Sin embargo, no está pensada como una plataforma de prueba sólida.

**¿Dónde se ejecutan los filtros de timbre de privilegios?**

Los filtros se ejecutan en el anillo 3, aunque algunos filtros controlan los dispositivos de streaming que se ejecutan en anillo 0. Para obtener más información, vea [Cómo participan los dispositivos de hardware en el gráfico de filtro](how-hardware-devices-participate-in-the-filter-graph.md).

**¿Es necesario usar un depurador de kernel?**

Depende de su proyecto específico. La instalación de las bibliotecas en tiempo de ejecución de depuración de DirectX significa que está instalando controladores de depuración y otros componentes de modo kernel, y que si la aplicación provoca una aserción de depuración en uno de estos componentes, el equipo se reiniciará automáticamente a menos que tenga un depurador de kernel asociado al proceso.

**Cuando ejecuto mi aplicación en el depurador, se bloquea.**

Algunos descodificadores están diseñados para no funcionar mientras la aplicación está asociada al depurador. Intente ejecutar la aplicación fuera del depurador.

**¿Cómo funciona la macro de definición de \_ GUID?**

La macro **definir \_ GUID** resuelve el problema de declarar `extern` referencias a valores GUID en el código fuente. Por ejemplo, supongamos que el proyecto tiene tres archivos de código fuente, Src1. cpp, Src2. cpp y Src3. cpp, y los tres archivos usan un determinado valor de GUID que ha definido. El valor GUID debe definirse exactamente una vez en el proyecto y los otros archivos de código fuente deben declarar `extern` referencias a él. Con la macro **definir \_ GUID** , puede usar el mismo archivo de encabezado para ambos propósitos. En el archivo de encabezado, declare el GUID de la siguiente manera:


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



(Si este ejemplo tiene ceros, coloque los valores reales de GUID). Puede usar la utilidad Guidgen.exe para crear un nuevo GUID y pegarlo en el archivo de encabezado en el formato de **\_ GUID de definición** . Incluya este archivo de encabezado en cada archivo de código fuente que haga referencia al GUID. En exactamente uno de los archivos de código fuente, incluya el archivo de encabezado Initguid. h delante del archivo de encabezado. Por ejemplo:


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



Siempre que no se incluya el archivo de encabezado Initguid. h, la macro **definir \_ GUID** crea una `extern` referencia al valor GUID. Cuando se incluye el archivo de encabezado Initguid. h, se vuelve a definir la macro **definir \_ GUID** para que **definir \_ GUID** cree una declaración de definición del GUID.

Si no incluye Initguid. h en ninguno de los archivos de código fuente, obtendrá un error de vínculo "símbolo externo sin resolver". Si incluye dos veces Initguid. h para el mismo GUID, obtendrá un error de compilación "redefinición; inicialización múltiple ". Para resolver estos errores, asegúrese de que Initguid. h se incluye exactamente una vez. Además, no incluya Initguid. h dentro de un archivo de encabezado precompilado, porque en efecto el encabezado precompilado se incluye en todos los archivos de código fuente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción a DirectShow](introduction-to-directshow.md)
</dt> </dl>

 

 




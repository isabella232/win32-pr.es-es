---
title: API de gráficos en Windows
description: En este artículo se describen las características y las API de gráficos de Windows.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7543ee7c5e3cdbfb022cc9299dd5ddd3cdd36981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421264"
---
# <a name="graphics-apis-in-windows"></a>API de gráficos en Windows

Windows Vista incluye compatibilidad con un modelo de controlador de pantalla totalmente nuevo que representa una revisión importante en el diseño de los controladores de vídeo desde la introducción del Modelo de controlador de Windows (WDM) para Windows 98. Este modelo rediseñado refleja la evolución del hardware de vídeo del mundo de las operaciones de tramas 2D y de las aplicaciones GDI en el de juegos 3D con hardware gráfico de función fija y, finalmente, de la unidad de procesamiento de gráficos (GPU) programable moderna que admite una amplia gama de aplicaciones de gráficos de alto rendimiento. Windows 7 y Windows 8 se basan en la infraestructura de gráficos de Windows Vista proporcionando API y características de gráficos adicionales. En este artículo se describen las características y las API de gráficos de Windows.

-   [Información preliminar](#background)
-   [Direct3D 9](#direct3d-9)
-   [9Ex de Direct3D](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10,1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11,1](#direct3d-111)
-   [OpenGL](#opengl)
-   [Compatibilidad de aplicaciones, GDI y versiones anteriores de Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Recomendaciones](#recommendations)

## <a name="background"></a>Información previa

La API principal para programar gráficos desde los primeros días de Windows era la interfaz gráfica de dispositivo (GDI). Esta API se ha diseñado para controlar numerosos dispositivos de salida 2D y ha formado la base para la experiencia de la interfaz de usuario de Windows. DirectDraw y Direct3D se introdujeron como API alternativas para admitir juegos de pantalla completa y representación 3D como extensiones para el hardware existente del tiempo. Las interacciones con GDI eran complicadas. Este diseño ha limitado la mezcla efectiva de los elementos GDI tradicionales con los elementos de Direct3D. La versión de Windows XP de WDM, conocida como XPDM, refleja la naturaleza en paralelo de GDI y Direct3D (vea la ilustración 1).

**Figura 1. API de gráficos en Windows XP**

![XPDM](images/graphics-apis-in-windows-xp.gif)

A lo largo de los años, la eficacia de las tarjetas de vídeo 3D ha crecido drásticamente hasta el punto en que la inmensa mayoría del hardware está dedicada a esta función. Un nuevo modelo de controladores, Windows Display Driver Model (WDDM), trae la GPU y Direct3D a Forefront, lo que permite la creación de una experiencia completamente nueva, el escritorio 3D, que combina sin problemas el mundo 2D de GDI con la eficacia de las GPU programables modernas. Con WDDM, el hardware de vídeo está completamente controlado por Direct3D y todas las demás interfaces de gráficos se comunican con el hardware de vídeo a través del nuevo modelo de controlador centrado en Direct3D (consulte la figura 2).

**Figura 2. API de gráficos en Windows Vista**

![WDDM](images/graphics-apis-in-windows-vista.gif)

Para obtener más información acerca del WDDM, vea [Guía de diseño del modelo de controladores de pantalla de Windows Vista (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) en MSDN.

## <a name="direct3d-9"></a>Direct3D 9

La versión 9 de DirectX se lanzó por primera vez para Windows en 2002, con las actualizaciones posteriores en 2003 y 2004. Esta API representa una década de evolución de las tecnologías de DirectX, la introducción de modelos de programación de sombreador más eficaces para Direct3D y una madurez respaldada por miles de cargos de envío. Direct3D 9 es la interfaz de gráficos principal en Windows Vista. Sigue siendo la API ideal para escribir juegos 3D y aplicaciones que necesitan ejecutarse en la amplia gama de hardware existente y versiones de Windows. Los detalles del nuevo modelo de controlador están ocultos en las aplicaciones que usan las interfaces de Direct3D 9, pero, en segundo plano, el sistema operativo está aprovechando al máximo las nuevas capacidades para proporcionar una verdadera multitarea de la GPU, una administración más eficaz de los recursos y un rendimiento sólido.

Para garantizar la compatibilidad total con versiones anteriores de Windows, algunas peculiaridades del modelo de controlador anterior deben emularse incluso con el nuevo modelo de controladores de pantalla de Windows Vista. Por ejemplo, cuando una aplicación de pantalla completa pierde el foco, debe suponer que ha perdido todos los recursos de la memoria de vídeo (VRAM) y volver a cargar los que se crearon como recursos no administrados aunque el nuevo modelo de controladores controle los recursos de forma transparente sin expulsarlos del contexto del dispositivo. Incluso el concepto de un tipo de recurso administrado y predeterminado es específico del modelo de controlador anterior. Otro ejemplo es la expectativa de error cuando se asignan recursos no administrados (grupo predeterminado) que superan la cantidad de VRAM disponible, aunque el nuevo modelo de controlador puede proporcionar una cantidad casi ilimitada de memoria de vídeo virtual. Debido a estos requisitos, las aplicaciones Direct3D que se ejecutan en Windows Vista seguirán recibiendo estas condiciones de error. Por lo tanto, están limitadas en su capacidad de usar las interfaces básicas de Direct3D 9 para usar completamente algunas características del nuevo modelo de controlador.

Aunque los nuevos sistemas que se distribuyen con Windows Vista incluirán tarjetas de vídeo con controladores WDDM, y los nuevos controladores para una serie de tarjetas de vídeo populares se incluyen en el cuadro, Windows Vista sigue admitiendo la capacidad de usar controladores XPDM anteriores para las actualizaciones y las ediciones corporativas. En los sistemas que usan el modelo de controlador anterior, se deben usar las interfaces de Direct3D 9 y anteriores, y el funcionamiento del sistema de gráficos es muy similar al de Windows XP (Figura 1). WDDM es necesario para que las aplicaciones usen Direct3D 9Ex, Direct3D 10 y versiones posteriores.

## <a name="direct3d-9ex"></a>9Ex de Direct3D

La interfaz 9Ex de Direct3D proporciona acceso a una ligera extensión de la API de Direct3D 9 estándar que expone la asignación de recursos virtualizada, la nueva semántica de dispositivo perdida y otras características nuevas que están disponibles mientras se ejecutan en Windows Vista. Al crear este objeto extendido, la API de Direct3D 9 usa la nueva semántica y, por tanto, requiere que la aplicación use una lógica diferente (y, por consiguiente, rutas de acceso de código diferentes) para la creación de recursos, la administración y el control de errores para los nuevos tipos de condiciones. Esta API solo está disponible en Windows Vista y requiere controladores WDDM. Dado que Direct3D 9Ex usa una ruta de acceso de código de controlador y API independiente que Direct3D 9, la compatibilidad con esta API requiere casos de prueba adicionales para la aplicación.

La razón principal para crear la nueva API de Direct3D 9Ex era permitir el acceso completo a las nuevas capacidades de WDDM, a la vez que se mantiene la compatibilidad con las aplicaciones de Direct3D existentes. El nuevo escritorio 3D y muchas aplicaciones específicas de Windows Vista hacen uso de esta versión de Direct3D 9, pero no funcionan cuando se ejecutan en controladores XPDM antiguos. Dado que la API 9Ex de Direct3D no aparecerá nunca en versiones anteriores de Windows debido a la falta de compatibilidad con el WDDM, las interfaces estándar de Direct3D 9 cubren un conjunto mucho más amplio de sistemas. En el caso de las aplicaciones de alto rendimiento que pueden beneficiarse de la próxima generación de hardware de vídeo, la versión 10 completamente nueva de Direct3D proporciona muchas funcionalidades nuevas que no expone Direct3D 9Ex. Como resultado, para juegos y la mayoría de las demás aplicaciones, Direct3D 9 o Direct3D 10 es la API recomendada.

> [!Note]  
> El SDK de DirectX no proporciona ejemplos, encabezados o bibliotecas para la interfaz 9Ex de Direct3D. MSDN Library y Windows SDK (anteriormente conocido como Platform SDK) contienen la documentación, los encabezados y las bibliotecas disponibles.

 

Para obtener más información sobre Direct3D 9Ex, consulte [DirectX para Windows Vista](/previous-versions//ms681824(v=vs.85)) en MDSN.

## <a name="direct3d-10"></a>Direct3D 10

Para obtener el máximo partido del nuevo modelo de controlador de Windows Vista y el hardware de próxima generación, se ha creado una versión totalmente nueva de la API de Direct3D. Aunque WDDM elimina algunas de las limitaciones en cuanto al rendimiento en el sistema de gráficos existente, Direct3D 10 sigue quitando cuellos de botella de diseño en la API de Direct3D existente y simplifica considerablemente la tarea de programación de la GPU.

La nueva API elimina completamente todos los aspectos de la función fija, excepto algunos, y los reemplaza con construcciones programables y simplifica considerablemente la implementación interna. Los cientos de bits de capacidad en versiones anteriores de Direct3D se han eliminado completamente y se han reemplazado por un conjunto de funciones inclusivo y bien definido que solo tiene algunos escenarios de uso opcionales para formatos de recursos específicos. La creación y validación de recursos que consumen mucha CPU ahora tienen una semántica explícita en la nueva API. Esto permite un comportamiento de rendimiento mucho más predecible y reduce considerablemente la sobrecarga por dibujo. Los recursos se pueden volver a configurar en varios formatos para permitir un uso eficaz en varias fases, y el conjunto de características impone muchas menos restricciones en los escenarios de uso de los formatos. También hay nuevos formatos de textura de mapa normal comprimidos en bloques.

En la nueva API, las constantes de sombreador y el estado del dispositivo son recursos explícitos, lo que permite un almacenamiento en caché mucho más eficiente en el hardware y una validación de controladores muy simplificada. El modelo de sombreador programable se ha unificado en los sombreadores de vértices y píxeles, y ha sido más expresivo con un modelo de cálculo y un conjunto de operadores bien definidos. Además, se ha agregado una nueva fase de sombreador de geometría para que funcione en primitivos después de la fase del sombreador de vértices. Los resultados del trabajo de la GPU en las fases de sombreador de vértices y de geometría de la canalización se pueden transmitir a la RAM de vídeo para su reutilización, lo que permite la posibilidad de operaciones de GPU de varias fases extremadamente complejas con una interacción mínima de la CPU.

Todas estas mejoras permiten la tecnología de gráficos de próxima generación y amplían la capacidad de las aplicaciones para descargar trabajos en la GPU. La descarga permite la piel de caracteres más compleja basada en GPU, técnicas de transformación acelerada, generación de volúmenes sombra y extrusión, sistemas físicos y de partículas que son materiales totalmente basados en GPU y más complejos combinados en lotes de gran tamaño, procedimientos detallados, asignación de desplazamiento con seguimiento de rayos en tiempo real, generación de mapa de cubos de un solo paso y muchas más técnicas, todo ello sin perder recursos de CPU para aplicaciones más complejas.

Para proporcionar este nivel de innovación en Direct3D 10, el hardware anterior no se puede expresar como una implementación parcial de una nueva interfaz. Una tarjeta de vídeo es capaz de admitir todas las características nuevas o no es una tarjeta compatible con Direct3D 10. Por lo tanto, aunque Direct3D 9 podría impulsar el hardware de DirectX7-era con muchos bits de funcionalidad ausentes y limitaciones de uso, Direct3D 10 solo funciona en una nueva generación de tarjetas de vídeo. Para que una aplicación admita el hardware de vídeo más antiguo, también debe ser compatible con las interfaces de Direct3D 9. Las versiones futuras de Direct3D se compilarán en la versión 10 y se ampliarán a las nuevas versiones de la API, a la vez que se garantiza un superconjunto estricto de la funcionalidad de Direct3D 10.

Para obtener más información sobre Direct3D 10, vea [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="direct3d-101"></a>Direct3D 10,1

Windows Vista Service Pack 1 amplía la API de Direct3D 10 con Direct3D 10,1, que agrega interfaces opcionales y un modelo de sombreador adicional para admitir las nuevas características de hardware de las tarjetas de vídeo que admiten Direct3D 10,1. Todo el hardware que es capaz de admitir Direct3D 10,1 también es totalmente compatible con todas las características de Direct3D 10 y los desarrolladores de juegos pueden hacer uso de las características adicionales de Direct3D 10,1, cuando estén disponibles.

> [!Note]  
> Direct3D 10,1 es la API de gráficos que usa el escritorio de Windows 7.

 

> [!Note]  
> Windows 7 y la actualización de Windows Vista ([KB 971644](https://support.microsoft.com/kb/971644)) agregan compatibilidad con los niveles de características de DXGI 1,1, 10level9 y el dispositivo WARP10 a la API de Direct3D 10,1 existente.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 es compatible con una nueva revisión de Direct3D, Direct3D 11, basada en el diseño de la API de Direct3D 10,1. Entre las nuevas características de la API se incluyen la representación multiproceso y la creación de recursos, el sombreador de cálculo, la compatibilidad con los niveles de características de 10level9 y el dispositivo de representación de software de WARP10, y las nuevas características de hardware de clase de Direct3D 11, como la teselación con los sombreadores de dominio & y 5,0 BC7, y la vinculación dinámica de sombreador. La nueva API puede usar las tarjetas de vídeo de clase de Direct3D 10 y 10,1 existentes, algunas tarjetas de Direct3D 9 a través de los niveles de características de 10level9 con compatibilidad con características limitadas y las tarjetas de vídeo de la clase de Direct3D 11 de última generación.

Además de la API de Direct3D 11, Windows 7 incluye DXGI 1,1, Direct2D, DirectWrite y compatibilidad con controladores WDDM 1,1.

> [!Note]  
> Direct3D 11 y las API relacionadas también están disponibles como una actualización de Windows Vista (consulte [KB 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11,1

Windows 8 amplía la [API de Direct3D 11](#direct3d-11) con Direct3D 11,1. Direct3D 11,1 admite todo el hardware existente que sea compatible con los [niveles de características](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11, 10 \_ x y 9 \_ x, así como un nuevo \_ nivel de características 11 1.

Además de la [API de Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features), Windows 8 incluye [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [contextos de dispositivo de DIRECT2D](/windows/desktop/Direct2D/devices-and-device-contexts)y compatibilidad con controladores WDDM 1,2.

> [!Note]  
> Si desea que las aplicaciones de la tienda Windows programen gráficos 3D con DirectX, puede usar la API de Direct3D 11,1. Para obtener más información sobre la programación de gráficos 3D con DirectX, vea [Introducción a los gráficos 3D con DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).

 

**Actualización de la plataforma para Windows 7:** La compatibilidad parcial está disponible para la [API de Direct3D 11,1](/windows/desktop/direct3d11/direct3d-11-1-features) en Windows 7 o windows Server 2008 R2 con la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838) instalada. Para obtener más información sobre la actualización de la plataforma para Windows 7, consulte [actualización de la plataforma para Windows 7](platform-update-for-windows-7.md).

## <a name="opengl"></a>OpenGL

Windows Vista, Windows 7 y Windows 8 proporcionan la misma compatibilidad que Windows XP para OpenGL, que permite a los fabricantes de tarjetas de vídeo proporcionar un controlador de cliente instalable (ICD) para OpenGL que proporciona compatibilidad con hardware. Tenga en cuenta que se requieren las versiones más recientes de estos ICDs para que sea totalmente compatible con Windows Vista, Windows 7 o Windows 8. Si no hay ningún ICD instalado, el sistema revertirá a la capa de software OpenGL v 1.1 en la mayoría de los casos.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Compatibilidad de aplicaciones, GDI y versiones anteriores de Direct3D

Los sistemas de gráficos de Windows Vista, Windows 7 y Windows 8 están diseñados para admitir una amplia gama de escenarios de hardware y uso para habilitar la nueva tecnología a la vez que continúan siendo compatibles con los sistemas existentes. Las interfaces de gráficos existentes, como GDI, GDI+ y versiones anteriores de Direct3D, siguen funcionando en Windows Vista y Windows 7, pero se reasignan internamente siempre que sea posible. Esto significa que la mayoría de las aplicaciones Windows existentes seguirán funcionando.

Windows Vista, Windows 7 y Windows 8 continúan admitiendo las mismas interfaces de Direct3D y DirectDraw que Windows XP, de vuelta a la versión 3 de DirectX (a excepción del modo retenido Direct3D's, que se ha quitado). Al igual que con Windows XP Professional x64 Edition, las aplicaciones nativas de 64 bits en las versiones más recientes de Windows se limitan a Direct3D9, DirectDraw7 o las interfaces más recientes. Las aplicaciones de alto rendimiento deben usar Direct3D 9 o posterior para asegurarse de que tienen la coincidencia más cercana con las capacidades de hardware.

## <a name="recommendations"></a>Recomendaciones

Tenga en cuenta las siguientes recomendaciones al seleccionar una API para la aplicación gráfica:

-   Use Direct3D 9 Si la aplicación debe admitir Windows XP o una versión anterior de Windows.
-   Use Direct3D 9 Si quiere que Windows Vista o Windows 7 se ejecuten con controladores XPDM. En el caso de los sistemas Windows Vista o Windows 7 que no tienen Direct3D 10 o un hardware de vídeo mejor, puede optar por usar la ruta de acceso del código de Windows XP Direct3D 9 existente o usar los niveles de características de 10level9 a través de la API Direct3D 10,1 o Direct3D 11.
-   Use Direct3D 11 para aprovechar las ventajas de la próxima generación de hardware de vídeo en Windows Vista, Windows 7 y Windows 8. Las aplicaciones de la tienda Windows deben usar Direct3D 11 o posterior.

 

 
---
title: API de gráficos en Windows
description: En este artículo se Windows características y API de gráficos.
ms.assetid: 54cd5027-cdcf-fc4a-40a9-beacfaa08681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848f24c42aa98c6d27a0873ab07c389dea24826d880188837536d83bd87549b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987168"
---
# <a name="graphics-apis-in-windows"></a>API de gráficos en Windows

Windows Vista incluye compatibilidad con un modelo de controlador de pantalla completamente nuevo que representa una revisión importante en el diseño de controladores de vídeo desde la introducción del modelo de controlador de Windows (WDM) para Windows 98. Este modelo rediseñado refleja la evolución del hardware de vídeo del mundo de las operaciones de trama 2D y las aplicaciones GDI a la de los juegos 3D con hardware gráfico de función fija y, por último, a la de la unidad de procesamiento de gráficos programable (GPU) moderna que admite una amplia gama de aplicaciones gráficas de alto rendimiento. Windows 7 y Windows 8 se basa en la infraestructura de gráficos Windows Vista proporcionando características y API de gráficos adicionales. En este artículo se Windows características y API de gráficos.

-   [Información preliminar](#background)
-   [Direct3D 9](#direct3d-9)
-   [Direct3D 9Ex](#direct3d-9ex)
-   [Direct3D 10](#direct3d-10)
-   [Direct3D 10.1](#direct3d-101)
-   [Direct3D 11](#direct3d-11)
-   [Direct3D 11.1](#direct3d-111)
-   [Opengl](#opengl)
-   [Compatibilidad de aplicaciones, GDI y versiones anteriores de Direct3D](#application-compatibility-gdi-and-older-versions-of-direct3d)
-   [Recomendaciones](#recommendations)

## <a name="background"></a>Información previa

La API principal para programar gráficos desde los primeros Windows ha sido la interfaz gráfica de dispositivo (GDI). Esta API se diseñó para controlar numerosos dispositivos de salida 2D y constituyeron la base de la experiencia Windows interfaz de usuario. DirectDraw y Direct3D se introdujeron como API alternativas para admitir juegos de pantalla completa y representación en 3D como extensiones del hardware existente de la época. Las interacciones con GDI eran complicadas. Este diseño ha limitado la mezcla eficaz de elementos GDI tradicionales con elementos Direct3D. La Windows XP de WDM, conocida como XPDM, refleja la naturaleza en paralelo de GDI y Direct3D (consulte la figura 1).

**Figura 1. API de gráficos en Windows XP**

![xpdm](images/graphics-apis-in-windows-xp.gif)

A lo largo de los años, la potencia de las tarjetas de vídeo 3D ha aumentado drásticamente hasta el punto en que la gran mayoría del hardware se dedica a esta función. Un nuevo modelo de controlador, Windows Display Driver Model (WDDM), pone la GPU y Direct3D a la vanguardia, lo que permite crear una experiencia completamente nueva, el escritorio 3D, que combina sin problemas el mundo 2D de GDI con la potencia de las GPU programables modernas. Con WDDM, el hardware de vídeo está controlado por completo por Direct3D y todas las demás interfaces gráficas se comunican con el hardware de vídeo a través del nuevo modelo de controlador centrado en Direct3D (consulte la figura 2).

**Figura 2. API de gráficos en Windows Vista**

![Wddm](images/graphics-apis-in-windows-vista.gif)

Para obtener más información sobre WDDM, vea Windows Guía de diseño del modelo de controlador de pantalla [de Vista (WDDM)](/windows-hardware/drivers/display/windows-vista-display-driver-model-design-guide) en MSDN.

## <a name="direct3d-9"></a>Direct3D 9

La versión 9 de DirectX se publicó por primera vez para Windows en 2002, con actualizaciones posteriores en 2003 y 2004. Esta API representa una década de evolución de las tecnologías de DirectX, la introducción de modelos de programación de sombreadores más eficaces para Direct3D y una madurez con el respaldo de miles de títulos de envío. Direct3D 9 es la interfaz gráfica principal en Windows Vista. Sigue siendo la API ideal para escribir juegos y aplicaciones en 3D que deben ejecutarse en la amplia gama de hardware y versiones Windows existentes. Los detalles del nuevo modelo de controlador están ocultos en las aplicaciones que usan las interfaces de Direct3D 9, pero en segundo plano el sistema operativo aprovecha al máximo las nuevas funcionalidades para proporcionar verdaderas tareas múltiples de la GPU, una administración de recursos más eficaz y un rendimiento sólido.

Para garantizar la compatibilidad completa con las versiones anteriores de Windows, algunas de las características del modelo de controlador anterior se deben emular incluso con el nuevo modelo de controlador de pantalla Windows Vista. Por ejemplo, cuando una aplicación de pantalla completa pierde el foco, debe suponer que ha perdido todos los recursos de la memoria de vídeo (VRAM) y volver a cargar los que creó como recursos no administrados, aunque el nuevo modelo de controlador controle los recursos de forma transparente sin expulsarlos del contexto del dispositivo. Incluso el concepto de un tipo de recurso administrado frente al predeterminado es específico del modelo de controlador anterior. Otro ejemplo es la expectativa de error al asignar recursos no administrados (grupo predeterminado) por encima de la cantidad de VRAM disponible, aunque el nuevo modelo de controlador puede proporcionar una cantidad casi ilimitada de memoria de vídeo virtual. Debido a estos requisitos, las aplicaciones de Direct3D que se ejecutan en Windows Vista seguirán recibiendo estas condiciones de error. Por lo tanto, están limitados en su capacidad de usar las interfaces básicas de Direct3D 9 para usar completamente algunas características del nuevo modelo de controlador.

Aunque los nuevos sistemas de envío con Windows Vista incluirán tarjetas de vídeo con controladores WDDM y se incluyen nuevos controladores para una serie de tarjetas de vídeo populares en la caja, Windows Vista sigue dando soporte a la capacidad de usar controladores XPDM más antiguos para actualizaciones y ediciones corporativas. En sistemas que usan el modelo de controlador anterior, se deben usar Direct3D 9 y interfaces anteriores, y el funcionamiento del sistema de gráficos es muy similar al de Windows XP (figura 1). WDDM es necesario para que las aplicaciones usen Direct3D 9Ex, Direct3D 10 y versiones posteriores.

## <a name="direct3d-9ex"></a>Direct3D 9Ex

La interfaz Direct3D 9Ex proporciona acceso a una pequeña extensión de la API estándar de Direct3D 9 que expone la asignación de recursos virtualizados, la nueva semántica de dispositivos perdidos y algunas otras características nuevas disponibles mientras se ejecuta en Windows Vista. Al crear este objeto extendido, la API de Direct3D 9 usa la nueva semántica y, por tanto, requiere que la aplicación use una lógica diferente (y, por tanto, rutas de acceso de código diferentes) para la creación, administración y control de errores de recursos para nuevos tipos de condiciones. Esta API solo está disponible en Windows Vista y requiere controladores WDDM. Dado que Direct3D 9Ex usa una RUTA de acceso de código de controlador y API independiente que Direct3D 9, la compatibilidad con esta API requiere casos de prueba adicionales para la aplicación.

La razón principal para crear la nueva API de Direct3D 9Ex era permitir el acceso completo a las nuevas funcionalidades de WDDM al tiempo que se mantiene la compatibilidad con las aplicaciones existentes de Direct3D. El nuevo escritorio 3D y muchas aplicaciones específicas de Windows Vista usan esta versión de Direct3D 9, pero no son funcionales cuando se ejecutan en controladores XPDM más antiguos. Dado que la API de Direct3D 9Ex nunca aparecerá en versiones anteriores de Windows debido a la falta de compatibilidad con WDDM, las interfaces estándar de Direct3D 9 cubren un conjunto mucho más amplio de sistemas. En el caso de las aplicaciones de alto rendimiento que pueden aprovechar la próxima generación de hardware de vídeo, la nueva versión 10 de Direct3D proporciona muchas funcionalidades nuevas que Direct3D 9Ex no expone. Como resultado, para juegos y la mayoría de las demás aplicaciones, Direct3D 9 o Direct3D 10 es la API recomendada.

> [!Note]  
> El SDK de DirectX no proporciona ejemplos, encabezados ni bibliotecas para la interfaz Direct3D 9Ex. MSDN Library y Windows SDK (anteriormente conocido como SDK de plataforma) contienen la documentación, los encabezados y las bibliotecas disponibles.

 

Para obtener más información sobre Direct3D 9Ex, vea [DirectX para Windows Vista](/previous-versions//ms681824(v=vs.85)) en MDSN.

## <a name="direct3d-10"></a>Direct3D 10

Para obtener el potencial del nuevo modelo de controlador Windows Vista y el hardware de próxima generación, se ha creado una versión completamente nueva de la API de Direct3D. Aunque WDDM elimina algunas de las limitaciones de rendimiento en el sistema de gráficos existente, Direct3D 10 va más allá mediante la eliminación de cuellos de botella de diseño en la API de Direct3D existente y simplifica enormemente la tarea de programar la GPU.

La nueva API elimina completamente todos los aspectos de función fija, pero algunos, y los reemplaza por construcciones programables y agigi la implementación interna. Los cientos de bits de funcionalidad de versiones anteriores de Direct3D se han eliminado por completo y se han reemplazado por un conjunto de funcionalidades inclusivo y bien definido que solo tiene algunos escenarios de uso opcionales para formatos de recursos específicos. La creación y validación de recursos que consumen mucha CPU ahora tienen semántica explícita en la nueva API. Esto permite un comportamiento de rendimiento mucho más predecible y una sobrecarga por dibujo muy reducida. Los recursos se pueden volver a configurar en varias formas para permitir un uso eficaz en varias fases, y el conjunto de características impone muchas menos restricciones en escenarios de uso para formatos. También hay nuevos formatos de textura de mapa normal comprimidos en bloque.

En la nueva API, las constantes del sombreador y el estado del dispositivo son recursos explícitos, lo que permite un almacenamiento en caché mucho más eficaz en el hardware y una validación del controlador muy simplificada. El modelo de sombreador programable se ha unificado en los sombreadores de vértices y píxeles, y se ha hecho más expresivo con un modelo de cálculo y un conjunto de operadores bien definidos. Además, se ha agregado una nueva fase del sombreador de geometría para operar en primitivas después de la fase del sombreador de vértices. Los resultados del trabajo de la GPU en las fases del sombreador de vértices y geometría de la canalización se pueden transmitir a la RAM de vídeo para su reutilización, lo que permite la posibilidad de operaciones de GPU de varios pasos extremadamente complejas con una interacción mínima de la CPU.

Todas estas mejoras permiten la tecnología de gráficos de próxima generación y amplían la capacidad de las aplicaciones para desactivar la carga del trabajo en la GPU. La descarga permite un descamblamiento de caracteres basado en GPU más complejo, técnicas de transformación acelerada, generación y extrusión de volúmenes de sombra, sistemas de partícula y física totalmente basados en GPU, materiales más complejos combinados en lotes eficaces de dibujo grande, detalles de procedimientos, asignación de desplazamientos con seguimiento de rayos en tiempo real, generación de mapa de cubo de paso único y muchas más técnicas, todo ello al tiempo que se liberan recursos de CPU para aplicaciones más complejas.

Para proporcionar este nivel de innovación en Direct3D 10, el hardware anterior no se puede expresar como una implementación parcial de una nueva interfaz. Una tarjeta de vídeo es capaz de admitir todas las características nuevas o no es una tarjeta compatible con Direct3D 10. Por lo tanto, aunque Direct3D 9 podría impulsar hardware de la era DirectX7 con muchos bits de funcionalidad y limitaciones de uso que faltan, Direct3D 10 solo funciona en una nueva generación de tarjetas de vídeo. Para que una aplicación admita hardware de vídeo anterior, también debe admitir las interfaces de Direct3D 9. Las versiones futuras de Direct3D se basarán en la versión 10, lo que la ampliará a las nuevas versiones de la API y garantizará un superconjunto estricto de funcionalidad de Direct3D 10.

Para obtener más información sobre Direct3D 10, [vea Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics).

## <a name="direct3d-101"></a>Direct3D 10.1

Windows Vista Service Pack 1 amplía la API de Direct3D 10 con Direct3D 10.1, que agrega interfaces opcionales y un modelo de sombreador adicional para admitir nuevas características de hardware de tarjetas de vídeo que admiten Direct3D 10.1. Todo el hardware capaz de admitir Direct3D 10.1 también es totalmente compatible con todas las características de Direct3D 10 y los desarrolladores de juegos pueden usar las características adicionales de Direct3D 10.1, cuando estén disponibles.

> [!Note]  
> Direct3D 10.1 es la API de gráficos que usa Windows escritorio 7.

 

> [!Note]  
> Windows 7 y la actualización de Windows Vista[(KB 971644)](https://support.microsoft.com/kb/971644)agregan compatibilidad con los niveles de características DXGI 1.1, 10level9 y el dispositivo WARP10 a la API existente de Direct3D 10.1.

 

## <a name="direct3d-11"></a>Direct3D 11

Windows 7 admite una nueva revisión de Direct3D, Direct3D 11, que se basa en el diseño de la API de Direct3D 10.1. Entre las nuevas características de la API se incluyen la representación multiproceso y la creación de recursos, el sombreador de proceso, la compatibilidad con niveles de características de 10 niveles9 y el dispositivo de representación de software WARP10, y las nuevas características de hardware de clase Direct3D 11, como la teselación mediante sombreadores de dominio de hull &, los formatos de compresión de textura BC6H y BC7, el modelo de sombreador 5.0 y la vinculación dinámica del sombreador. La nueva API puede usar tarjetas de vídeo existentes de las clases Direct3D 10 y 10.1, algunas tarjetas Direct3D 9 a través de los niveles de características de 10 niveles 9 con compatibilidad limitada con características y las tarjetas de vídeo de clase Direct3D 11 de última generación.

Además de la API de Direct3D 11, Windows 7 incluye DXGI 1.1, Direct2D, DirectWrite y compatibilidad con controladores WDDM 1.1.

> [!Note]  
> Direct3D 11 y las API relacionadas también están disponibles como una actualización de Windows Vista (consulte [KB 971644](https://support.microsoft.com/kb/971644)).

 

## <a name="direct3d-111"></a>Direct3D 11.1

Windows 8 la [API de Direct3D 11](#direct3d-11) con Direct3D 11.1. Direct3D 11.1 admite todo el hardware existente que admite los niveles [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) características 11, 10 x y 9 x, así como un nuevo nivel de \_ característica \_ \_ 11 1.

Además de la [API de Direct3D 11.1,](/windows/desktop/direct3d11/direct3d-11-1-features)Windows 8 incluye [DXGI 1.2,](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)contextos de dispositivo [Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts)y compatibilidad con controladores WDDM 1.2.

> [!Note]  
> Si desea que las Windows Store programe gráficos 3D con DirectX, puede usar la API de Direct3D 11.1. Para obtener más información sobre la programación de gráficos 3D con DirectX, consulte Introducción a [los gráficos 3D con DirectX.](/previous-versions/windows/apps/hh465137(v=win.10))

 

**Actualización de plataforma para Windows 7:** La compatibilidad parcial está disponible para la API de [Direct3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features) en Windows 7 o Windows Server 2008 R2 con la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838) instalada. Para obtener más información sobre la actualización de plataforma para Windows 7, vea Actualización de plataforma [para Windows 7](platform-update-for-windows-7.md).

## <a name="opengl"></a>Opengl

Windows Vista, Windows 7 y Windows 8 proporcionan la misma compatibilidad que Windows XP para OpenGL, lo que permite a los fabricantes de tarjetas de vídeo proporcionar un controlador cliente (ICD) instalable para OpenGL que proporciona compatibilidad acelerada por hardware. Tenga en cuenta que las versiones más recientes de estos TIC son necesarias para admitir completamente Windows Vista, Windows 7 o Windows 8. Si no hay ningún ICD instalado, el sistema volverá a la capa de software OpenGL v1.1 en la mayoría de los casos.

## <a name="application-compatibility-gdi-and-older-versions-of-direct3d"></a>Compatibilidad de aplicaciones, GDI y versiones anteriores de Direct3D

Los sistemas de gráficos Windows Vista, Windows 7 y Windows 8 están diseñados para admitir una amplia gama de escenarios de hardware y uso con el objetivo de habilitar nuevas tecnologías a la vez que se siguen manteniendo los sistemas existentes. Las interfaces gráficas existentes, como GDI, GDI+ y versiones anteriores de Direct3D, siguen funcionando en Windows Vista y Windows 7, pero se reemergen internamente siempre que sea posible. Esto significa que la mayoría de las aplicaciones Windows existentes seguirán funcionando.

Windows Vista, Windows 7 y Windows 8 siguen siendo compatibles con las mismas interfaces Direct3D y DirectDraw que Windows XP, de vuelta a la versión 3 de DirectX (a excepción del modo retenido de Direct3D, que se ha quitado). Al igual que con Windows XP Professional x64 Edition, las aplicaciones nativas de 64 bits en versiones más recientes de Windows se limitan a las interfaces Direct3D9, DirectDraw7 o más recientes. Las aplicaciones de alto rendimiento deben usar Direct3D 9 o posterior para asegurarse de que tienen la mejor coincidencia con las funcionalidades de hardware.

## <a name="recommendations"></a>Recomendaciones

Tenga en cuenta las siguientes recomendaciones al seleccionar una API para la aplicación gráfica:

-   Use Direct3D 9 si la aplicación debe admitir Windows XP o una versión anterior de Windows.
-   Use Direct3D 9 si desea admitir Windows Vista o Windows 7 que se ejecutan con controladores XPDM. Para los sistemas Windows Vista o Windows 7 que carecen de hardware de vídeo Direct3D 10 o superior, puede optar por usar la ruta de acceso de código existente de Windows XP Direct3D 9 o usar los niveles de características de 10 niveles9 a través de la API direct3D 10.1 o Direct3D 11.
-   Use Direct3D 11 para aprovechar la próxima generación de hardware de vídeo en Windows Vista, Windows 7 y Windows 8. Windows Las aplicaciones de la Tienda deben usar Direct3D 11 o posterior.

 

 
---
description: En esta documentación se hace referencia específicamente a las extensiones de Windows Vista para gráficos de DirectX.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Resumen de características (Direct3D 9 para Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cf2447297b7f24edf7d0200e640d5aef90bff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696076"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Resumen de características (Direct3D 9 para Windows Vista)

En esta documentación se hace referencia específicamente a las extensiones de Windows Vista para gráficos de DirectX. Para desarrollar el potencial de DirectX para Windows Vista, debe instalar el SDK de Windows Vista, así como el SDK de DirectX. Las aplicaciones que usan DirectX para Windows Vista deben usar hardware que use el controlador WDDM (modelo de controladores de dispositivos de Windows) en lugar de XPDM (modelo de controladores de XP). los controladores que no implementan el WDDM no pueden crear instancias de las interfaces de gráficos DirectX de Windows Vista.

Descubra las nuevas características de gráficos de DirectX en Windows Vista en una de estas secciones:

-   [Cambios de comportamiento del dispositivo](#device-behavior-changes)
-   [Deshabilitar el procesamiento de vértices de software multiproceso](#disabling-multithreaded-software-vertex-processing)
-   [Superficies de un bit](#one-bit-surfaces)
-   [Lectura de búferes de profundidad/estarcido](#reading-depthstencil-buffers)
-   [Compartir recursos](#sharing-resources)
-   [Conversión sRGB antes de la fusión](#srgb-conversion-before-blending)
-   [Mejoras de StretchRect](#stretchrect-improvements)
-   [Creación de texturas en la memoria del sistema](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Cambios de comportamiento del dispositivo

Los dispositivos ahora solo se pierden en dos circunstancias: Cuando se restablece el hardware porque está bloqueado y cuando se detiene el controlador de dispositivo. Cuando se bloquea el hardware, se puede restablecer el dispositivo mediante una llamada a [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex). Si el hardware se bloquea, se pierde la memoria de la textura.

Una vez detenido un controlador, el objeto IDirect9Ex debe volver a crearse para reanudar la representación.

Cuando el área de presentación está oscurecida por otra ventana en modo de ventana, o cuando una aplicación de pantalla completa está minimizada, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) devolverá S \_ D3DPRESENTATIONOCCLUDED. Las aplicaciones de pantalla completa pueden reanudar la representación cuando reciben un mensaje de devolución de llamada de [**WM \_ ACTIVATEAPP**](../winmsg/wm-activateapp.md) .

En versiones anteriores de DirectX, cuando una aplicación experimentó un cambio de modo, la única manera de recuperarlo era restablecer el dispositivo y volver a crear todos los recursos de memoria de vídeo y cadenas de intercambio. Ahora con DirectX para Windows Vista, al llamar a Reset después de un cambio de modo no se pierden las superficies de la memoria de textura, las texturas y la información de estado, y no es necesario volver a crear estos recursos.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Deshabilitar el procesamiento de vértices de software multiproceso

Se ha agregado un nuevo bit de Cap (D3DCREATE \_ Disable \_ PSGP \_ Threading) que deshabilitará el multithreading para el procesamiento de vértices de software (SWVP). Use esta macro para generar una marca de comportamiento para IDirect3D9:: CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Superficies de un bit

Hay un nuevo tipo de formato de superficie de un bit que puede ser especialmente útil para procesar glifos de texto. El nuevo formato se denomina D3DFMT \_ a1. Una superficie de un bit está diseñada para usarse como una textura por píxel o como la salida de destino de representación generada por ComposeRects o ColorFill. No hay ningún Cap independiente para el ancho y el alto de la superficie. una implementación de debe admitir una superficie de tamaño único que sea 2K textura x 8K textura.

Una superficie de un bit tiene un bit por textura; por lo tanto, una de ellas significa que todos los componentes (r, g, b, a) de un píxel son 1 y cero, lo que significa que todos los componentes son iguales a 0. Puede usar superficies de un bit con las siguientes API: ColorFill, UpdateSurface y UpdateTexture.

Cuando se lee una superficie de un bit, el tiempo de ejecución puede realizar cualquier ejemplo de punto o filtrado de circunvolución. El filtro de convolución es ajustable (vea [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Existen algunas restricciones para las superficies de un bit:

-   No se admite la asignación de MIP
-   los datos sRGB no se pueden leer ni escribir en una superficie de un bit.
-   No se puede usar una superficie de un bit como textura de vértices ni para el muestreo múltiple.

## <a name="reading-depthstencil-buffers"></a>Lectura de búferes de profundidad/estarcido

Use IDirect3DDevice9:: UpdateSurface para leer o escribir datos de profundidad/estarcido de las superficies obtenidas de IDirect3DDevice9:: CreateDepthStencilSurface o IDirect3DDevice9:: GetDepthStencilSurface.

En primer lugar, cree una superficie solo bloqueable, solo de profundidad o de galería de símbolos con IDirect3DDevice9:: CreateOffscreenPlainSurface. Use uno de los formatos siguientes:

-   D3DFMT \_ D16 \_ bloqueable
-   D3DFMT \_ D32F \_ bloqueable
-   D3DFMT \_ D32 \_ bloqueable
-   D3DFMT \_ S8 \_ bloqueable

En segundo lugar, se transfieren datos entre el búfer de profundidad/estarcido y la profundidad de la galería de símbolos o la profundidad que se acaba de crear. La transferencia se realiza mediante IDirect3DDevice9:: UpdateSurface.

Se producirá un error en UpdateSurface cuando ambas superficies tengan un formato de BLOQUEable o ambos no se puedan bloquear.

La transferencia de datos inexistentes producirá un error (por ejemplo, transferir desde una superficie solo de profundidad no bloqueable a una \_ superficie bloqueada de S8 de D3DFMT \_ ).

El resto de las restricciones de IDirect3DDevice9:: UpdateSurface se siguen aplicando.

## <a name="sharing-resources"></a>Compartir recursos

Los recursos de Direct3D ahora se pueden compartir entre dispositivos o procesos. Esto se aplica a cualquier recurso de Direct3D, como texturas, búferes de vértices, búferes de índice o superficies (como destinos de representación, búferes de estarcido de profundidad o superficies sin formato de pantalla). Para compartirlo, debe designar un recurso para compartir en el momento de la creación y ubicar el recurso en el grupo predeterminado (D3DPOOL \_ predeterminado). Una vez que se crea un recurso para el uso compartido, se puede compartir entre los dispositivos de un proceso o compartir entre los procesos.

Para habilitar los recursos compartidos, las API de creación de recursos tienen un parámetro de identificador adicional. Se trata de un identificador que apunta al recurso compartido. En revisiones anteriores de DirectX, este argumento formaba parte de la firma de la API, pero se ha desusado y debe establecerse en **null**. A partir de Windows Vista, use pSharedHandle de las siguientes maneras:

-   Establezca el puntero (pSharedHandle) en **null** para no compartir un recurso. Esto es igual que el comportamiento de DirectX anterior a Windows Vista.
-   Para crear un recurso compartido, llame a cualquier API de creación de recursos (consulte a continuación) con un identificador no inicializado (el propio puntero no es **null** (pSharedHandle! = **null**), pero el puntero señala a un valor **null** ( \* pSharedHandle = = **null**)). La API generará un recurso compartido y devolverá un identificador válido.
-   Para abrir y obtener acceso a un recurso compartido creado previamente mediante un identificador de recurso compartido no nulo, establezca pSharedHandle en la dirección de ese identificador. Después de abrir el recurso compartido creado previamente de esta manera, puede usar la interfaz devuelta en la API Direct3D 9 o Direct3D 9Ex como si la interfaz fuera un recurso típico de ese tipo.

Las API de creación de recursos incluyen- [**CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface**](/windows/desktop/api), [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)y [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Existen algunas restricciones en el uso de recursos compartidos. Entre ellas se incluyen las siguientes:

-   La API que se usa para abrir un recurso compartido debe coincidir con la API que se usó para crear el recurso compartido. Por ejemplo, si ha utilizado [**CreateTexture**](/windows/desktop/api) para crear un recurso compartido, debe usar **CreateTexture** para abrir ese recurso compartido. Si usó [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) para crear un recurso compartido, debe usar **CreateRenderTarget** para abrir ese recurso compartido, etc.
-   Al abrir un recurso compartido, debe especificar el \_ valor predeterminado de D3DPOOL.
-   Los recursos bloqueable (texturas con búferes \_ dinámicos de D3DUSAGE, de vértices y de índice, por ejemplo) pueden experimentar un rendimiento deficiente cuando se comparten. No se podrá compartir el Rendertargets bloqueable en algún hardware.
-   Las referencias a un recurso compartido de proceso cruzado deben tener las mismas dimensiones que el recurso original. Al pasar un identificador en todo el proceso, incluya la información de la dimensión para que se pueda crear la referencia de forma idéntica.
-   Las superficies entre procesos compartidas no proporcionan ningún mecanismo de sincronización. Es posible que los cambios de lectura/escritura en una superficie compartida no reflejen la vista de un proceso de referencia de la superficie cuando se espera. Para proporcionar la sincronización, use las consultas de eventos o bloquee la textura.
-   Solo el proceso que crea inicialmente un recurso compartido puede bloquearlo (cualquier proceso que abra una referencia a ese recurso compartido no puede bloquearlo).
-   Si un recurso compartido está bloqueado, no hay ninguna validación para que otros procesos sepan si el recurso está disponible.

## <a name="srgb-conversion-before-blending"></a>Conversión sRGB antes de la fusión

Ahora puede comprobar para ver si el dispositivo puede convertir los datos de canalización en sRGB antes de la combinación de búferes de fotogramas. Esto implica que el dispositivo convierte los valores Render-target de sRGB. Para ver si el hardware admite la conversión, compruebe este límite:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Este extremo identifica el hardware que admite la conversión a sRGB antes de la fusión. Esta capacidad es importante para la representación de alta calidad de los búferes de fotogramas de FP16 en el administrador de ventanas de escritorio (DWM).

## <a name="stretchrect-improvements"></a>Mejoras de StretchRect

En versiones anteriores de DirectX, StretchRect tiene muchas restricciones para acomodar diferentes controladores (consulte IDirect3DDevice9:: StretchRect). Windows Vista se basa en el modelo de controladores de dispositivos de Windows (WDDM). Este nuevo modelo de controladores es mucho más robusto y permite que los controladores controlen casos especiales en el hardware.

En general, la única restricción restante es que el destino de representación se debe haber creado con el uso de destino de representación (D3DUSAGE \_ RENDERTARGET). Esta restricción se eleva si va a realizar una copia simple (donde el origen y el destino tienen el mismo formato, el mismo tamaño y no hay ningún rectángulo).

## <a name="texture-creation-in-system-memory"></a>Creación de texturas en la memoria del sistema

Las aplicaciones que necesitan más flexibilidad sobre el uso, la asignación y la eliminación de la memoria del sistema ahora pueden crear texturas a partir de un puntero de memoria del sistema. Por ejemplo, una aplicación podría crear una textura de Direct3D a partir de un puntero de mapa de bits de memoria del sistema GDI.

Debe hacer dos cosas para crear este tipo de textura:

-   Asigne suficiente memoria del sistema para almacenar la superficie de textura. El número mínimo de bytes es el ancho x alto x bytes por píxel.
-   Pase la dirección de un puntero a la superficie de memoria del sistema para el parámetro de identificador \* a IDirect3DDevice9:: CreateTexture.

Este es el prototipo de función para IDirect3DDevice9:: CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Una textura de memoria del sistema tiene las restricciones siguientes:

-   El paso de textura debe ser igual al ancho de la textura multiplicado por el número de bytes por píxel.
-   Cuando se usan formatos comprimidos (formatos DXT), la aplicación es responsable de asignar el tamaño correcto.
-   Solo se admiten texturas con un solo nivel de mipmap.
-   El valor pasado a CreateTexture para el argumento Pool debe ser D3DPOOL \_ SYSTEMMEM.
-   Esta API encapsula la memoria suministrada en una textura. No Desasigne esta memoria hasta que haya terminado.

 

 

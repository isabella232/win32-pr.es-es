---
description: Esta documentación hace referencia específicamente a las extensiones Windows Vista para gráficos DirectX.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: Resumen de características (Direct3D 9 para Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242af80fa4d6f00c1e55d4852884f9fbbf8de287c6792b3b4aaaad196a6cd113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523083"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>Resumen de características (Direct3D 9 para Windows Vista)

Esta documentación hace referencia específicamente a las extensiones Windows Vista para gráficos DirectX. Para desarrollar la potencia de DirectX para Windows Vista, debe instalar el SDK de Windows Vista, así como el SDK de DirectX. Las aplicaciones que usan DirectX para Windows Vista deben usar hardware que use el controlador WDDM (modelo de controlador de dispositivo Windows) en lugar del XPDM (modelo de controlador XP); Los controladores que no implementan WDDM no pueden crear instancias Windows interfaces gráficas de DirectX de Vista.

Descubra las nuevas características de gráficos de DirectX Windows Vista en una de estas secciones:

-   [Cambios de comportamiento del dispositivo](#device-behavior-changes)
-   [Deshabilitar el procesamiento de vértices de software multiproceso](#disabling-multithreaded-software-vertex-processing)
-   [Superficies de un bit](#one-bit-surfaces)
-   [Profundidad de lectura/búferes de galería de símbolos](#reading-depthstencil-buffers)
-   [Uso compartido de recursos](#sharing-resources)
-   [Conversión de sRGB antes de combinar](#srgb-conversion-before-blending)
-   [Mejoras de StretchRect](#stretchrect-improvements)
-   [Creación de texturas en la memoria del sistema](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Cambios de comportamiento del dispositivo

Los dispositivos ahora solo se pierden en dos circunstancias; cuando se restablece el hardware porque está en suspensión y cuando se detiene el controlador del dispositivo. Cuando el hardware se desajuste, se puede restablecer el dispositivo mediante una llamada [**a ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex). Si el hardware se para, se pierde la memoria de textura.

Una vez detenido un controlador, se debe volver a crear el objeto IDirect9Ex para reanudar la representación.

Cuando otra ventana oculta el área de presentación en modo de ventana o cuando se minimiza una aplicación de pantalla completa, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) devolverá S \_ D3DPRESENTATIONOCCLUDED. Las aplicaciones de pantalla completa pueden reanudar la representación cuando reciben un mensaje de devolución de [**\_ llamada DE WM ACTIVATEAPP.**](../winmsg/wm-activateapp.md)

En versiones anteriores de DirectX, cuando una aplicación experimentaba un cambio de modo, la única manera de recuperar era restablecer el dispositivo y volver a crear todos los recursos de memoria de vídeo y las cadenas de intercambio. Ahora, con DirectX para Windows Vista, llamar a Reset después de un cambio de modo no hace que se pierdan las superficies de la memoria de textura, las texturas y la información de estado, y no es necesario volver a crear estos recursos.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Deshabilitar el procesamiento de vértices de software multiproceso

Se ha agregado un nuevo bit de límites (D3DCREATE DISABLE PSGP THREADING) que deshabilitará el multithreading para el procesamiento de vértices de \_ \_ software \_ (swvp). Use esta macro para generar una marca de comportamiento para IDirect3D9::CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Superficies de un bit

Hay un nuevo tipo de formato de superficie de un bit que puede ser especialmente útil para procesar glifos de texto. El nuevo formato se denomina D3DFMT \_ A1. Una superficie de un bit está diseñada para usarse como textura por píxel o la salida de destino de representación generada por ComposeRects o ColorFill. No hay límites independientes para el ancho y el alto de la superficie; una implementación debe admitir una superficie de tamaño único que sea 2K texels x 8K texels.

Una superficie de un bit tiene un bit por texel; por lo tanto, uno significaría que todos los componentes (r,g,b,a) de un píxel son 1 y cero significaría que todos los componentes son iguales a 0. Puede usar superficies de un bit con las siguientes API: ColorFill, UpdateSurface y UpdateTexture.

Cuando se lee una superficie de un bit, el tiempo de ejecución puede realizar el filtrado de muestras de punto o de convolución. El filtro de convolución es ajustable (vea [**SetConvolutionMonoKernel).**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)

Existen algunas restricciones para las superficies de un bit:

-   No se admite la asignación de mip
-   Los datos sRGB no se pueden leer ni escribir en una superficie de un bit.
-   Una superficie de un bit no se puede usar como textura de vértice ni para multimuestreo.

## <a name="reading-depthstencil-buffers"></a>Profundidad de lectura/búferes de galería de símbolos

Use IDirect3DDevice9::UpdateSurface para leer o escribir datos de profundidad o galería de símbolos de superficies obtenidas de IDirect3DDevice9::CreateDepthStencilSurface o IDirect3DDevice9::GetDepthStencilSurface.

En primer lugar, cree una superficie que solo se puede bloquear, solo de profundidad o de galería de símbolos mediante IDirect3DDevice9::CreateOffscreenPlainSurface. Use uno de los formatos siguientes:

-   D3DFMT \_ D16 \_ LOCKABLE
-   D3DFMT \_ D32F \_ LOCKABLE
-   D3DFMT \_ D32 \_ LOCKABLE
-   D3DFMT \_ S8 \_ LOCKABLE

En segundo lugar, transfiera datos entre el búfer de profundidad o galería de símbolos y la superficie de galería de símbolos o profundidad que se puede bloquear recién creada. La transferencia se realiza mediante IDirect3DDevice9::UpdateSurface.

UpdateSurface producirá un error cuando ambas superficies tienen un formato LOCKABLE o ambas no se pueden bloquear.

La transferencia de datos inexistentes producirá un error (por ejemplo, la transferencia de una superficie de solo profundidad no bloqueable a una superficie D3DFMT \_ S8 \_ LOCKABLE).

El resto de restricciones para IDirect3DDevice9::UpdateSurface todavía se aplican.

## <a name="sharing-resources"></a>Uso compartido de recursos

Los recursos de Direct3D ahora se pueden compartir entre dispositivos o procesos. Esto se aplica a cualquier recurso de Direct3D, incluidas texturas, búferes de vértices, búferes de índice o superficies (como destinos de representación, búferes de galería de símbolos de profundidad o superficies sin formato fuera de la pantalla). Para compartirlo, debe designar un recurso para compartirlo en el momento de la creación y buscar el recurso en el grupo predeterminado (D3DPOOL \_ DEFAULT). Una vez que se crea un recurso para compartirlo, se puede compartir entre dispositivos dentro de un proceso o entre procesos.

Para habilitar los recursos compartidos, las API de creación de recursos tienen un parámetro de identificador adicional. Se trata de un identificador que apunta al recurso compartido. En revisiones anteriores de DirectX, este argumento formaba parte de la firma de API, pero no se ha usado y debe establecerse en **NULL.** A partir Windows Vista, use pSharedHandle de las maneras siguientes:

-   Establezca el puntero (pSharedHandle) en **NULL** para no compartir un recurso. Esto es igual que el comportamiento de DirectX antes de Windows Vista.
-   Para crear un recurso compartido, llame a cualquier API de creación de recursos (consulte a continuación) con un identificador sin inicializar (el propio puntero no es **NULL** (pSharedHandle != **NULL),** pero el puntero apunta a un valor **NULL** ( \* pSharedHandle == **NULL**)). La API generará un recurso compartido y devolverá un identificador válido.
-   Para abrir y acceder a un recurso compartido creado previamente mediante un identificador de recursos compartidos que no sea DEULL, establezca pSharedHandle en la dirección de ese identificador. Después de abrir el recurso compartido creado anteriormente de esta manera, puede usar la interfaz devuelta en direct3D 9 o Direct3D 9Ex API como si la interfaz fuera un recurso típico de ese tipo.

Las API de creación de recursos [**incluyen: CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture,**](/windows/desktop/api) [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface,**](/windows/desktop/api) [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateDepthStencilSurfaceEx,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex) [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)y [**CreateRenderTargetEx.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex)

Hay algunas restricciones para usar recursos compartidos. Estos incluyen las siguientes:

-   La API que use para abrir un recurso compartido debe coincidir con la API que usó para crear el recurso compartido. Por ejemplo, si usó [**CreateTexture para**](/windows/desktop/api) crear un recurso compartido, debe usar **CreateTexture** para abrir ese recurso compartido. Si usó [**CreateRenderTarget para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) crear un recurso compartido, debe usar **CreateRenderTarget** para abrir ese recurso compartido, y así sucesivamente.
-   Al abrir un recurso compartido, debe especificar D3DPOOL \_ DEFAULT.
-   Los recursos que se pueden bloquear (texturas con D3DUSAGE DYNAMIC, búferes de vértices y búferes de índice, por ejemplo) pueden experimentar un rendimiento deficiente \_ cuando se comparten. Los elementos rendertarget que se pueden bloquear no se compartirán en algún hardware.
-   Las referencias a un recurso compartido entre procesos deben tener las mismas dimensiones que el recurso original. Al pasar un identificador a través del proceso, incluya la información de dimensión para que la referencia se pueda crear de forma idéntica.
-   Las superficies entre procesos compartidos no proporcionan ningún mecanismo de sincronización. Es posible que los cambios de lectura y escritura en una superficie compartida no reflejen la vista de la superficie de un proceso de referencia cuando se espera. Para proporcionar sincronización, use consultas de eventos o bloquee la textura.
-   Solo el proceso que crea inicialmente un recurso compartido puede bloquearlo (cualquier proceso que abra una referencia a ese recurso compartido no puede bloquearlo).
-   Si un recurso compartido está bloqueado, no hay ninguna validación para que otros procesos sepan si el recurso está disponible.

## <a name="srgb-conversion-before-blending"></a>Conversión de sRGB antes de combinar

Ahora puede comprobar si el dispositivo puede convertir datos de canalización en sRGB antes de la combinación de búfer de fotogramas. Esto implica que el dispositivo convierte los valores de destino de representación de sRGB. Para ver si el hardware admite la conversión, compruebe este límite:


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Este límite identifica el hardware que admite la conversión a sRGB antes de la combinación. Esta funcionalidad es importante para la representación de alta calidad de los búferes de fotogramas fp16 en el administrador de ventanas de escritorio (DWM).

## <a name="stretchrect-improvements"></a>Mejoras de StretchRect

En versiones anteriores de DirectX, StretchRect tiene muchas restricciones para alojar controladores diferentes (vea IDirect3DDevice9::StretchRect). Windows Vista se basa en Windows Device Driver Model (WDDM). Este nuevo modelo de controlador es mucho más sólido y permite a los controladores controlar casos especiales en el hardware.

En general, la única restricción restante es que el destino de representación se debe haber creado con el uso de destino de representación (D3DUSAGE \_ RENDERTARGET). Esta restricción se eleva si está realizando una copia simple (donde el origen y el valor de dest tienen el mismo formato, el mismo tamaño y no hay sub rectángulos).

## <a name="texture-creation-in-system-memory"></a>Creación de texturas en la memoria del sistema

Las aplicaciones que necesitan más flexibilidad sobre el uso, la asignación y la eliminación de la memoria del sistema ahora pueden crear texturas a partir de un puntero de memoria del sistema. Por ejemplo, una aplicación podría crear una textura direct3D a partir de un puntero de mapa de bits de memoria del sistema GDI.

Debe hacer dos cosas para crear una textura de este tipo:

-   Asigne suficiente memoria del sistema para contener la superficie de textura. El número mínimo de bytes es width x height x bytes por píxel.
-   Pase la dirección de un puntero a la superficie de memoria del sistema para el parámetro HANDLE \* a IDirect3DDevice9::CreateTexture.

Este es el prototipo de función para IDirect3DDevice9::CreateTexture:


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Una textura de memoria del sistema tiene las restricciones siguientes:

-   El tono de textura debe ser igual al ancho de textura por el número de bytes por píxel.
-   Cuando se usan formatos comprimidos (formatos DXT), la aplicación es responsable de asignar el tamaño correcto.
-   Solo se admiten texturas con un solo nivel de mapa mip.
-   El valor pasado a CreateTexture para el argumento Pool debe ser D3DPOOL \_ SYSTEMMEM.
-   Esta API encapsula la memoria proporcionada en una textura. No desasigne esta memoria hasta que haya terminado con ella.

 

 

---
title: Uso compartido de la superficie entre las API de gráficos de Windows
description: En este tema se proporciona información general técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794223"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Uso compartido de la superficie entre las API de gráficos de Windows

En este tema se proporciona información general técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex. Si ya tiene conocimientos prácticos de estas API, este documento puede ayudarle a usar varias API para representarlas en la misma superficie en una aplicación diseñada para los sistemas operativos Windows 7 o Windows Vista. En este tema también se proporcionan instrucciones de prácticas recomendadas y punteros a recursos adicionales.

> [!Note]  
> Para la interoperabilidad de Direct2D y DirectWrite en el tiempo de ejecución de DirectX 11,1, puede usar [dispositivos y contextos de dispositivo de direct2d](/windows/desktop/Direct2D/devices-and-device-contexts) para representarlos directamente en dispositivos de Direct3D 11.

 

En este tema se incluyen las siguientes secciones.

-   [Introducción](#introduction)
-   [Información general sobre la interoperabilidad de API](#api-interoperability-overview)
-   [Escenarios de interoperabilidad](#interoperability-scenarios)
    -   [Uso compartido de dispositivos de Direct3D 10,1 con Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [Superficies compartidas de DXGI 1,1 sincronizadas](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Conclusión](#conclusion)

## <a name="introduction"></a>Introducción

En este documento, la interoperabilidad de la API de gráficos de Windows hace referencia al uso compartido de la misma superficie de representación en distintas API. Este tipo de interoperabilidad permite a las aplicaciones crear pantallas atractivas aprovechando varias API de gráficos de Windows y facilitar la migración a nuevas tecnologías manteniendo la compatibilidad con las API existentes.

En Windows 7 (y Windows Vista SP2 con Windows 7 Interop Pack, vista 7IP), las API de representación de gráficos son Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9C y las API de Direct3D anteriores, así como GDI y GDI+. Windows Imaging Component (WIC) y DirectWrite son tecnologías relacionadas con el procesamiento de imágenes y Direct2D realiza la representación de texto. DirectX video Acceleration API (DXVA), basado en Direct3D 9C y Direct3D 9Ex, se usa para el procesamiento de vídeo.

A medida que las API de gráficos de Windows evolucionan hasta estar basadas en Direct3D, Microsoft está invirtiendo más en garantizar la interoperabilidad entre las API. Las API de Direct3D que se acaban de desarrollar y las API de nivel superior basadas en las API de Direct3D también proporcionan compatibilidad cuando es necesario para la compatibilidad de puente con las API anteriores. Para ilustrar, las aplicaciones de Direct2D pueden usar Direct3D 10,1 compartiendo un dispositivo Direct3D 10,1. Además, las API de Direct3D 11, Direct2D y Direct3D 10,1 pueden aprovechar las ventajas de la infraestructura de gráficos de DirectX (DXGI) 1,1, que permite que las superficies compartidas sincronizadas sean totalmente compatibles con la interoperabilidad entre estas API. Las API basadas en DXGI 1,1 interoperan con GDI y con GDI+ por asociación mediante la obtención del contexto de dispositivo GDI desde una superficie de DXGI 1,1. Para obtener más información, consulte la documentación de interoperabilidad de DXGI y GDI disponible en MSDN.

El uso compartido de la superficie sin sincronizar es compatible con el tiempo de ejecución de Direct3D 9Ex. Las aplicaciones de vídeo basadas en DXVA pueden usar la aplicación auxiliar de interoperabilidad de Direct3D 9Ex y DXGI para la interoperabilidad de los DXVA basados en 9Ex de Direct3D con Direct3D 11 para el sombreador de cálculo, o pueden interoperar con Direct2D para controles 2D o representación de texto. WIC y DirectWrite también interoperan con GDI, Direct2D y por asociación y otras API de Direct3D.

Direct3D 10,0, Direct3D 9C y los tiempos de ejecución de Direct3D más antiguos no admiten superficies compartidas. Las copias de memoria del sistema se seguirán usando para la interoperabilidad con las API basadas en GDI o en DXGI.

Tenga en cuenta que los escenarios de interoperabilidad de este documento hacen referencia a varias API de gráficos que se representan en una superficie de representación compartida, en lugar de en la misma ventana de la aplicación. La sincronización de API independientes que tienen como destino diferentes superficies que se componen en la misma ventana está fuera del ámbito de este documento.

## <a name="api-interoperability-overview"></a>Información general sobre la interoperabilidad de API

La interoperabilidad del uso compartido de Surface de las API de gráficos de Windows se puede describir en términos de escenarios de API a API y la funcionalidad de interoperabilidad correspondiente. A partir de Windows 7 y a partir de Windows Vista SP2 con 7IP, las nuevas API y los tiempos de ejecución asociados incluyen Direct2D y tecnologías relacionadas: Direct3D 11 y DXGI 1,1. También se ha mejorado el rendimiento de GDI en Windows 7. Direct3D 10,1 se presentó en Windows Vista SP1. En el diagrama siguiente se muestra la compatibilidad de interoperabilidad entre las API.

![diagrama de compatibilidad de interoperabilidad entre las API de gráficos de Windows](images/surface-sharing-interoperability.png)

En este diagrama, las flechas muestran escenarios de interoperabilidad en los que las API conectadas pueden tener acceso a la misma superficie. Las flechas azules indican mecanismos de interoperabilidad introducidos en Windows Vista. Las flechas verdes indican compatibilidad de interoperabilidad con nuevas API o mejoras que ayudan a las API más antiguas a interoperar con las API más recientes. Por ejemplo, las flechas verdes representan el uso compartido de dispositivos, la compatibilidad con superficies compartidas sincronizadas, la aplicación auxiliar de sincronización Direct3D 9Ex/DXGI y la obtención de un contexto de dispositivo GDI desde una superficie compatible.

## <a name="interoperability-scenarios"></a>Escenarios de interoperabilidad

A partir de Windows 7 y Windows Vista 7IP, las ofertas estándar de las API de gráficos de Windows admiten varias API que se representan en la misma superficie de DXGI 1,1.

**Direct3D 11, Direct3D 10,1, Direct2D: interoperabilidad entre sí**

Las API de Direct3D 11, Direct3D 10,1 y Direct2D (y sus API relacionadas como DirectWrite y WIC) pueden interoperar entre sí mediante el uso compartido de dispositivos Direct3D 10,1 o las superficies compartidas sincronizadas.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Uso compartido de dispositivos de Direct3D 10,1 con Direct2D

El uso compartido de dispositivos entre Direct2D y Direct3D 10,1 permite que una aplicación use ambas API para representar sin problemas y de forma eficaz en la misma superficie de DXGI 1,1, con el mismo objeto de dispositivo Direct3D subyacente. Direct2D proporciona la capacidad de llamar a las API de Direct2D mediante un dispositivo Direct3D 10,1 existente, aprovechando el hecho de que Direct2D se basa en los tiempos de ejecución de Direct3D 10,1 y DXGI 1,1. En los fragmentos de código siguientes se muestra cómo Direct2D obtiene el destino de representación del dispositivo Direct3D 10,1 de una superficie de DXGI 1,1 asociada con el dispositivo. El destino de representación del dispositivo Direct3D 10,1 puede ejecutar llamadas de dibujo de Direct2D entre las API BeginDraw y EndDraw.


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



**Comentarios:**

-   El dispositivo Direct3D 10,1 asociado debe admitir el formato BGRA. Dicho dispositivo se creó mediante una llamada a D3D10CreateDevice1 con el parámetro D3D10 \_ Create \_ Device \_ BGRA \_ support. El formato BGRA se admite a partir del nivel de características 9,1 de Direct3D 10.
-   La aplicación no debe crear varios ID2D1RenderTargets que se asocien al mismo dispositivo de Direct3D 10.1.
-   Para obtener un rendimiento óptimo, mantenga al menos un recurso en todo momento, como texturas o superficies asociadas al dispositivo.

El uso compartido de dispositivos es apto para el uso en proceso de un solo subproceso de un dispositivo de representación compartido por las API de representación de Direct3D 10,1 y Direct2D. Las superficies compartidas sincronizadas habilitan el uso de varios subprocesos, en proceso y fuera de proceso de varios dispositivos de representación usados por las API de Direct3D 10,1, Direct2D y Direct3D 11.

Otro método de interoperabilidad de Direct3D 10,1 y Direct2D es mediante ID3D1RenderTarget:: CreateSharedBitmap, que crea un objeto ID2D1Bitmap a partir de IDXGISurface. Puede escribir una escena de Direct3D 10.1 en el mapa de bits y representarla con Direct2D. Para obtener más información, vea [ID2D1RenderTarget:: CreateSharedBitmap Method](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).

### <a name="direct2d-software-rasterization"></a>Rasterización de software de Direct2D

El uso compartido de dispositivos con Direct3D 10,1 no se admite cuando se usa el representador de software de Direct2D, por ejemplo, mediante la especificación de D2D1 \_ presentación de \_ destino \_ \_ forzar representación \_ \_ de software en D2D1 \_ representar \_ el uso de destino \_ al crear un destino de representación de Direct2D.

Direct2D puede usar el rasterizador de software WARP10 para compartir dispositivos con Direct3D 10 o Direct3D 11, pero el rendimiento disminuye considerablemente.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>Superficies compartidas de DXGI 1,1 sincronizadas

Las API de Direct3D 11, Direct3D 10,1 y Direct2D usan DXGI 1,1, que proporciona la funcionalidad para sincronizar la lectura y la escritura en la misma superficie de memoria de vídeo (DXGISurface1) en dos o más dispositivos de Direct3D. Los dispositivos de representación que usan superficies compartidas sincronizadas pueden ser dispositivos de Direct3D 10,1 o Direct3D 11, cada uno de los cuales se ejecuta en el mismo proceso o en procesos cruzados.

Las aplicaciones pueden usar superficies compartidas sincronizadas para interoperar entre cualquier dispositivo basado en DXGI 1,1, como Direct3D 11 y Direct3D 10,1, o entre Direct3D 11 y Direct2D, obteniendo el dispositivo Direct3D 10,1 del objeto de destino de representación de Direct2D.

En Direct3D 10,1 y las API de versiones posteriores, para usar DXGI 1,1, asegúrese de que el dispositivo Direct3D se crea con un objeto de adaptador de DXGI 1,1, que se enumera desde el objeto de fábrica de DXGI 1,1. Llame a CreateDXGIFactory1 para crear el objeto IDXGIFactory1 y EnumAdapters1 para enumerar el objeto IDXGIAdapter1. El objeto IDXGIAdapter1 debe pasarse como parte de la llamada a D3D10CreateDevice o D3D10CreateDeviceAndSwapChain. Para obtener más información sobre las API de DXGI 1,1, consulte la [Guía de programación para dxgi](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>API existentes

**\_Recurso \_ compartido D3D10 \_ varios \_ KEYEDMUTEX**  
Al crear el recurso compartido Synchronized, establezca el \_ recurso D3D10 \_ \_ Shared \_ KEYEDMUTEX en la \_ marca D3D10 Resource \_ Misc \_ .  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**\_Recurso \_ compartido D3D10 \_ varios \_ KEYEDMUTEX**  
Permite que el recurso creado se sincronice con las API IDXGIKeyedMutex:: AcquireSync y ReleaseSync. Las siguientes API de Direct3D 10,1 de creación de recursos que toman un \_ parámetro de marca de varios recursos D3D10 se han \_ \_ ampliado para admitir la nueva marca.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1::CreateBuffer

  
Si se llama a cualquiera de las funciones enumeradas con \_ el \_ \_ conjunto de indicadores compartidos de KEYEDMUTEX de recursos D3D10 \_ , se puede consultar la interfaz devuelta para una interfaz IDXGIKeyedMutex, que implementa las API AcquireSync y ReleaseSync para sincronizar el acceso a la superficie. El dispositivo que crea la superficie y cualquier otro dispositivo que abra la superficie (mediante OpenSharedResource) es necesario para llamar a IDXGIKeyedMutex:: AcquireSync antes que cualquier comando de representación a la superficie y IDXGIKeyedMutex:: ReleaseSync cuando finaliza la representación.  
Los dispositivos de ALABEo y de referencia no admiten recursos compartidos. Si se intenta crear un recurso con esta marca en un dispositivo de ALABEo o de referencia, el método Create devolverá un \_ código de error E OUTOFMEMORY.  
**INTERFAZ IDXGIKEYEDMUTEX**  
Una nueva interfaz en DXGI 1,1, IDXGIKeyedMutex, representa una exclusión mutua con clave, que permite el acceso exclusivo a un recurso compartido que usan varios dispositivos. Para obtener documentación de referencia sobre esta interfaz y sus dos métodos, AcquireSync y ReleaseSync, consulte [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Ejemplo: uso compartido de superficies sincronizadas entre dos dispositivos de Direct3D 10,1

En el ejemplo siguiente se muestra cómo compartir una superficie entre dos dispositivos de Direct3D 10,1. La superficie compartida sincronizada se crea mediante un dispositivo Direct3D 10.1.


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



El mismo dispositivo Direct3D 10.1 puede obtener la superficie compartida sincronizada para la representación llamando a AcquireSync y, a continuación, liberando la superficie de la representación de otro dispositivo llamando a ReleaseSync. Cuando no se comparte la superficie compartida sincronizada con ningún otro dispositivo Direct3D, el creador puede obtener y liberar la superficie compartida sincronizada (para iniciar y finalizar la representación) adquiriendo y liberando con el mismo valor de clave.


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



El segundo dispositivo Direct3D 10.1 puede obtener la superficie compartida sincronizada para la representación llamando a AcquireSync y, a continuación, liberando la superficie de la representación del primer dispositivo mediante una llamada a ReleaseSync. Tenga en cuenta que el dispositivo 2 puede adquirir la superficie compartida sincronizada con el mismo valor de clave que el especificado en la llamada de ReleaseSync por dispositivo 1.


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



Los dispositivos adicionales que comparten la misma superficie pueden tomar la adquisición y liberación de la superficie mediante claves adicionales, como se muestra en las siguientes llamadas.


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



Tenga en cuenta que una aplicación real siempre puede representarse en una superficie intermedia que luego se copia en la superficie compartida para evitar que un dispositivo espere en otro dispositivo que comparta la superficie.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Usar superficies compartidas sincronizadas con Direct2D y Direct3D 11

Del mismo modo, para el uso compartido entre las API de Direct3D 11 y Direct3D 10,1, se puede crear una superficie compartida sincronizada desde cualquier dispositivo de API y compartirla con los otros dispositivos de la API, dentro o fuera del proceso.

Las aplicaciones que usan Direct2D pueden compartir un dispositivo Direct3D 10,1 y usar una superficie compartida sincronizada para interoperar con Direct3D 11 u otros dispositivos de Direct3D 10,1, tanto si pertenecen al mismo proceso como a procesos diferentes. Sin embargo, para las aplicaciones de un solo proceso y de un solo subproceso, el uso compartido de dispositivos es el método de interoperabilidad más eficaz y de alto rendimiento entre Direct2D y Direct3D 10 o Direct3D 11.

### <a name="software-rasterizer"></a>Rasterizador de software

Las superficies compartidas sincronizadas no se admiten cuando las aplicaciones usan los rasterizadores de software Direct3D o Direct2D, incluido el rasterizador de referencia y el ALABEo, en lugar de usar la aceleración de hardware de gráficos.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI

Las API de Direct3D 9Ex incluyen la noción de uso compartido de la superficie para permitir que otras API lean desde la superficie compartida. Para compartir la lectura y la escritura en una superficie compartida de Direct3D 9Ex, debe agregar la sincronización manual a la propia aplicación.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Superficies compartidas de Direct3D 9Ex más la aplicación auxiliar de sincronización manual

La tarea más fundamental de la interoperabilidad de Direct3D 9Ex y Direct3D 10 o 11 es pasar una sola superficie del primer dispositivo (dispositivo a) al segundo (dispositivo B), de modo que cuando el dispositivo B adquiera un identificador en la superficie, se garantice que la representación del dispositivo a se ha completado. Por lo tanto, el dispositivo B puede usar esta superficie sin preocuparse. Esto es muy similar al problema clásico productor-consumidor y este debate modela el problema de esa manera. El primer dispositivo que usa la superficie y después lo cede es el productor (dispositivo A) y el dispositivo que está esperando inicialmente es el consumidor (dispositivo B). Cualquier aplicación real es más sofisticada que esta y encadenará varios bloques de creación productor-consumidor para crear la funcionalidad deseada.

Los bloques de creación productor-consumidor se implementan en el ayudante mediante una cola de superficies. El productor pone en cola las superficies y las pone en cola el consumidor. La aplicación auxiliar presenta tres interfaces COM: ISurfaceQueue, ISurfaceProducer y ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>Información general de High-Level de la aplicación auxiliar

El objeto ISurfaceQueue es el bloque de creación para usar las superficies compartidas. Se crea con un dispositivo Direct3D inicializado y una descripción para crear un número fijo de superficies compartidas. El objeto Queue administra la creación de recursos y la apertura de código. El número y tipo de superficies son fijos. una vez creadas las superficies, la aplicación no las puede agregar ni quitar.

Cada instancia del objeto ISurfaceQueue proporciona una especie de calle unidireccional que se puede usar para enviar superficies desde el dispositivo productor al dispositivo de consumo. Se pueden usar varias calles unidireccionales para habilitar escenarios de uso compartido de superficie entre dispositivos de aplicaciones específicas.

**Creación/duración del objeto**  
Hay dos maneras de crear el objeto de cola: a través de CreateSurfaceQueue o mediante el método Clone de ISurfaceQueue. Dado que las interfaces son objetos COM, se aplica la administración de la duración de COM estándar.  
**Modelo productor/consumidor**  
Enqueue (): el productor llama a esta función para indicar que se ha realizado con la superficie, que ahora puede estar disponible para otro dispositivo. Al volver de esta función, el dispositivo productor ya no tiene derechos en la superficie y no es seguro seguir utilizándolo.  
Quitar de la cola (): el dispositivo consumidor llama a esta función para obtener una superficie compartida. La API garantiza que todas las superficies que se hayan quitado de la cola están listas para usarse.  
**Metadatos**  
La API admite la Asociación de metadatos con las superficies compartidas.  
Enqueue () tiene la opción de especificar metadatos adicionales que se pasarán al dispositivo de consumo. Los metadatos deben ser inferiores a un máximo conocido en el momento de la creación.  
La eliminación de la cola () puede pasar opcionalmente un búfer y un puntero al tamaño del búfer. La cola rellena el búfer con los metadatos de la llamada de puesta en cola correspondiente.  
**Clonación**  
Cada objeto ISurfaceQueue resuelve una sincronización unidireccional. Suponemos que la mayoría de las aplicaciones que usan esta API usarán un sistema cerrado. El sistema cerrado más sencillo con dos dispositivos que envían superficies hacia atrás y hacia delante requiere dos colas. El objeto ISurfaceQueue tiene un método Clone () para que sea posible crear varias colas que formen parte de la misma canalización mayor.  
Clone crea un nuevo objeto ISurfaceQueue a partir de uno existente y comparte todos los recursos abiertos entre ellos. El objeto resultante tiene exactamente las mismas superficies que la cola de origen. Las colas clonadas pueden tener distintos tamaños de metadatos entre sí.  
**Superficies**  
ISurfaceQueue asume la responsabilidad de crear y administrar sus superficies. No es válido poner en cola superficies arbitrarias. Además, una superficie solo debe tener un "propietario" activo. Debe estar en una cola específica o ser utilizada por un dispositivo específico. No es válido tener en varias colas o para que los dispositivos continúen usando la superficie después de ponerla en cola.  
</dl>

### <a name="api-details"></a>Detalles de la API

### <a name="isurfacequeue"></a>IsurfaceQueue

La cola es responsable de la creación y el mantenimiento de los recursos compartidos. También proporciona la funcionalidad para encadenar varias colas mediante Clone. La cola tiene métodos que abren el dispositivo productor y un dispositivo de consumo. Solo una de ellas se puede abrir en cualquier momento.

La cola expone las siguientes API:



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Crea un objeto ISurfaceQueue (la cola "raíz").                              |
| ISurfaceQueue::OpenConsumer | Devuelve una interfaz para el dispositivo de consumo que se va a quitar de la cola.                        |
| ISurfaceQueue::OpenProducer | Devuelve una interfaz para el dispositivo de producción que se va a poner en cola.                        |
| ISurfaceQueue:: Clone        | Crea un objeto ISurfaceQueue que comparte superficies con el objeto de cola raíz. |



 

**CreateSurfaceQueue**  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



**Miembros**  

**Ancho**, **alto**  las dimensiones de las superficies compartidas. Todas las superficies compartidas deben tener las mismas dimensiones.  
**Formato** Formato de las superficies compartidas. Todas las superficies compartidas deben tener el mismo formato. Los formatos válidos dependen de los dispositivos que se vayan a usar, ya que los distintos pares de dispositivos pueden compartir distintos tipos de formato.  
**NumSurfaces**  El número de superficies que forman parte de la cola. Se trata de un número fijo.  
 **MetaDataSize**  Tamaño máximo del búfer de metadatos.  
**Marcas**  de  Marcas para controlar el comportamiento de la cola. Vea la sección Comentarios.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parámetros**

 *pDesc* \[ en \]  la descripción de la cola de superficie compartida que se va a crear.  

 *pDevice* \[ en \]  el dispositivo que se debe usar para crear las superficies compartidas. Se trata de un parámetro explícito debido a una característica de Windows Vista. En el caso de las superficies compartidas entre Direct3D 9 y Direct3D 10, las superficies deben crearse con Direct3D 9.  

 *ppQueue* \[ fuera \]  de la devolución, contiene un puntero al objeto ISurfaceQueue.  


**Valores devueltos**

Si *pDevice* no es capaz de compartir recursos, esta función devuelve una \_ \_ llamada no válida de DXGI \_ . Esta función crea los recursos. Si se produce un error, devuelve un error. Si se realiza correctamente, devuelve S \_ correcto.

**Comentarios:**

Al crear el objeto de cola, también se crean todas las superficies. Se supone que todas las superficies son destinos de representación 2D y se crearán con el \_ destino de representación de enlace D3D10 y el conjunto de \_ \_ \_ \_ marcadores de recursos del sombreador de enlace D3D10 \_ (o las marcas equivalentes para los diferentes runtimes).

El desarrollador puede especificar una marca que indica si varios subprocesos tendrán acceso a la cola. Si no se establece ningún marcador (**Flags** = = 0), varios subprocesos usarán la cola. El desarrollador puede especificar el acceso de un solo subproceso, que desactiva el código de sincronización y proporciona una mejora del rendimiento para esos casos. Cada cola clonada tiene su propia marca, por lo que es posible que las distintas colas del sistema tengan controles de sincronización diferentes.

 **Apertura de un productor**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parámetros**  

*pDevice* \[ de\]  

El dispositivo productor que pone en cola las superficies en la cola de la superficie. 

*ppProducer* \[ out \] devuelve un objeto a la interfaz del productor.  


**Valores devueltos**

Si el dispositivo no es capaz de compartir superficies, devuelve un \_ error de DXGI \_ llamada no válida \_ .

**Apertura de un consumidor**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parámetros**  
 *pDevice* \[ de\]  
 El dispositivo de consumidor que quita las superficies de la cola de Surface. 
 *ppConsumer* \[ out \]  devuelve un objeto a la interfaz del consumidor.  


**Valores devueltos**

Si el dispositivo no es capaz de compartir superficies, devuelve un \_ error de DXGI \_ llamada no válida \_ .

**Comentarios:**

Esta función abre todas las superficies en la cola del dispositivo de entrada y las almacena en caché. Las llamadas subsiguientes a dequeue simplemente Irán a la memoria caché y no tendrán que volver a abrir las superficies cada vez.



### <a name="cloning-an-idxgixsurfacequeue"></a>Clonar un IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



**Los miembros** **MetaDataSize** y **Flags** tienen el mismo comportamiento que para CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parámetros**

*pDesc* \[ en \] una estructura que proporciona una descripción del objeto clonado que se va a crear. Este parámetro debe inicializarse.  
*ppQueue* \[ out \] devuelve el objeto inicializado.  
</dl>

**Comentarios:**

Puede clonar desde cualquier objeto de cola existente, incluso si no es la raíz.  
</dl>

### <a name="idxgixsurfaceconsumer"></a>IDXGIXSurfaceConsumer

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



**Parámetros**  
*ID.* \[ en\]  
REFIID de una superficie 2D del dispositivo de consumo.  

-   En el caso de una IDirect3DDevice9, REFIID debe ser \_ \_ Uuidof (IDirect3DTexture9).
-   En el caso de una ID3D10Device, REFIID debe ser \_ \_ Uuidof (ID3D10Texture2D).
-   En el caso de una ID3D11Device, REFIID debe ser \_ \_ Uuidof (ID3D11Texture2D).

*ppSurface* \[ out \] devuelve un puntero a la superficie.  
*pBuffer* \[ en, \] un parámetro opcional y, si no **es null**, en la devolución, contiene los metadatos que se pasaron en la llamada de enqueue correspondiente.  
*pBufferSize* \[ en, fuera \] del tamaño de *pBuffer*, en bytes. Devuelve el número de bytes devueltos en *pBuffer*. Si la llamada de puesta en cola no proporcionó metadatos, *pBuffer* se establece en 0.  
*dwTimeout* \[ en \] especifica un valor de tiempo de espera. Vea los comentarios para obtener más detalles.  
</dl>

**Valores devueltos**

Esta función puede devolver el tiempo \_ de espera si se especifica un valor de tiempo de espera y la función no devuelve antes del valor de tiempo de espera. Vea la sección Comentarios. Si no hay superficies disponibles, la función devuelve con *ppSurface* establecido en **null**, *pBufferSize* establecido en 0 y el valor devuelto es 0x80070120 (Win32 \_ a \_ HRESULT ( \_ tiempo de espera de espera)).  
</dl>

**Comentarios:**

Esta API se puede bloquear si la cola está vacía. El parámetro *dwTimeout* funciona de forma idéntica a las API de sincronización de Windows, como WaitForSingleObject. En el caso de un comportamiento sin bloqueo, utilice un tiempo de espera de 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Esta interfaz proporciona dos métodos que permiten a la aplicación poner en cola las superficies. Después de poner en cola una superficie, el puntero de Surface ya no es válido y no es seguro usarlo. La única acción que debe realizar la aplicación con el puntero es liberarla.



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer:: enqueue | Pone en cola una superficie en el objeto de cola. Una vez finalizada esta llamada, el productor se realiza con la superficie y la superficie está lista para otro dispositivo. |
| ISurfaceProducer:: Flush   | Se usa si las aplicaciones deben tener un comportamiento sin bloqueo. Para obtener información detallada, vea la sección Comentarios de.                                                                  |



 

**Poner en cola**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**Parámetros**  
*pSurface* \[ de\]  
Superficie del dispositivo de producción que se debe poner en cola. Esta superficie debe ser una superficie quitada de la cola de la misma red de cola. *pBuffer* \[ en \] un parámetro opcional, que se usa para pasar los metadatos. Debe apuntar a los datos que se pasarán a la llamada de eliminación de la cola.  
*BufferSize* \[ en \] el tamaño de *pBuffer*, en bytes.  
*Marcas* \[ de en \] un parámetro opcional que controla el comportamiento de esta función. La única marca es SURFACE \_ Queue \_ Flag \_ \_ no \_ espera. Vea los comentarios para el vaciado. Si no se pasa ninguna marca (*Flags* = = 0), se utiliza el comportamiento de bloqueo predeterminado.  
</dl>

**Valores devueltos**

Esta función puede devolver el \_ error \_ \_ de DXGI todavía se \_ está dibujando si se usa una marca de cola de superficie \_ \_ \_ \_ no \_ esperada.  
</dl>

**Comentarios:**

-   Esta función coloca la superficie en la cola. Si la aplicación no especifica que la \_ marca de la cola de Surface no \_ \_ \_ \_ espere, esta función está bloqueando y realizará una sincronización de CPU de GPU para asegurarse de que toda la representación en la superficie en cola está completa. Si esta función se ejecuta correctamente, habrá una superficie disponible para quitar de la cola. Si desea un comportamiento sin bloqueo, use la marca no \_ \_ esperar. Vea Flush () para obtener más información.
-   Según las reglas de recuento de referencias COM, la superficie devuelta por dequeue será AddRef (), por lo que la aplicación no necesita hacer esto. Después de llamar a enqueue, la aplicación debe liberar la superficie porque ya no la está usando.

**Vaciar**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parámetros**  
*Flags* \[in\]  
La única marca es SURFACE \_ Queue \_ Flag \_ \_ no \_ espera. Vea la sección Comentarios. *nSurfaces* \[ out \] devuelve el número de superficies que todavía están pendientes y no se han vaciado.  
</dl>

**Valores devueltos**

Esta función puede devolver \_ el error \_ \_ de DXGI todavía se \_ está dibujando si se usa la marca de la cola de Surface \_ \_ \_ \_ no \_ esperada. Esta función devuelve S \_ OK si alguna superficie se vació correctamente. Esta función devuelve el \_ error de DXGI \_ todavía se está \_ \_ dibujando si no se ha vaciado ninguna superficie. Juntos, el valor devuelto y *nSurfaces* indican a la aplicación qué trabajo se ha realizado y si queda algún trabajo.  
</dl>

**Comentarios:**

El vaciado solo es significativo si la llamada anterior a enqueue usó la \_ \_ marca no wait; de lo contrario, será una operación no operativa. Si la llamada a enqueue usó la \_ \_ marca no wait, enqueue se devuelve inmediatamente y no se garantiza la sincronización de la CPU de GPU. La superficie se considera todavía en cola, el dispositivo productor no puede seguir utilizándola, pero no está disponible para quitar de la cola. Para intentar confirmar la superficie de la eliminación de la cola, se debe llamar a Flush. Vaciar intenta confirmar todas las superficies que están actualmente en cola. Si no se pasa ninguna marca al vaciado, se bloqueará y se borrará toda la cola, y se prepararán todas las superficies en ella para quitar de la cola. Si \_ \_ se usa la marca no esperar, la cola comprobará las superficies para ver si alguna de ellas está lista; este paso no se bloquea. Las superficies que han terminado la GPU: la sincronización de CPU estará lista para el dispositivo de consumidor. Las superficies que siguen pendientes no se verán afectadas. La función devuelve el número de superficies que todavía es necesario vaciar.

> [!Note]  
> El vaciado no interrumpirá la semántica de la cola. La API garantiza que las superficies que se ponen en cola en primer lugar se confirmarán antes de que las superficies se ponen en cola más adelante, independientemente de Cuándo se produzca la sincronización de CPU-GPU.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Aplicación auxiliar de Direct3D 9Ex y DXGI Interop: Cómo usar

Esperamos que la mayoría de los casos de uso impliquen dos dispositivos que compartan varias superficies. Dado que este también es el escenario más sencillo, en este documento se detalla cómo usar las API para lograr este objetivo, se describe una variación de no bloqueo y finaliza con una breve sección sobre la inicialización de tres dispositivos.

### <a name="two-devices"></a>Dos dispositivos

La aplicación de ejemplo que usa este ayudante puede usar Direct3D 9Ex y Direct3D 11 juntos. La aplicación puede procesar el contenido con ambos dispositivos y presentar contenido mediante Direct3D 9. El procesamiento podría significar la representación de contenido, la descodificación de vídeo, la ejecución de sombreadores de cálculo, etc. En cada fotograma, la aplicación se procesará primero con Direct3D 11, después se procesará con Direct3D 9 y, por último, con Direct3D 9. Además, el procesamiento con Direct3D 11 generará algunos metadatos que debe consumir Direct3D 9. En esta sección se trata el uso de la aplicación auxiliar en tres partes que corresponden a esta secuencia: inicialización, bucle principal y limpieza.

**Inicialización**  
La inicialización consta de los siguientes pasos:  

1.  Inicialice ambos dispositivos.
2.  Cree la cola raíz: m \_ 11to9Queue.
3.  Clone desde la cola raíz: m \_ 9to11Queue.
4.  Llame a OpenProducer/OpenConsumer en ambas colas.

Los nombres de cola usan los números 9 y 11 para indicar qué API es el productor y cuál es el consumidor: **m \_ ***productor*** a cola de ***consumidores*****. En consecuencia, m \_ 11to9Queue indica una cola para la que el dispositivo Direct3D 11 genera superficies que el dispositivo de Direct3D 9 consume. Del mismo modo, m \_ 9to11Queue indica una cola para la que Direct3D 9 produce superficies que usa Direct3D 11.  
La cola raíz está inicialmente llena y todas las colas clonadas están inicialmente vacías. Esto no debería ser un problema para la aplicación, salvo el primer ciclo de las colas y las decolas y la disponibilidad de los metadatos. Si una eliminación de cola solicita metadatos, pero no se estableció ninguno (ya sea porque no hay nada inicialmente o la puesta en cola no estableció nada), la eliminación de la cola observa que no se recibieron metadatos.  

1.  **Inicialice ambos dispositivos.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Cree la cola raíz.**  
    En este paso también se crean las superficies. Las restricciones de tamaño y formato son idénticas a la creación de cualquier recurso compartido. El tamaño del búfer de metadatos se fija en el momento de la creación y, en este caso, solo pasaremos un UINT.  
    La cola se debe crear con un número fijo de superficies. El rendimiento variará en función del escenario. Tener varias superficies aumenta la probabilidad de que los dispositivos estén ocupados. Por ejemplo, si solo hay una superficie, no habrá ninguna paralelización entre los dos dispositivos. Por otro lado, el aumento del número de superficies aumenta la superficie de memoria, lo que puede reducir el rendimiento. En este ejemplo se usan dos superficies.  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  **Clone la cola raíz.**  
    Cada cola clonada debe usar las mismas superficies pero puede tener distintos tamaños de búfer de metadatos y marcas diferentes. En este caso, no hay metadatos de Direct3D 9 a Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Abra el productor y los dispositivos de consumidor.**  
    La aplicación debe realizar este paso antes de llamar a poner en cola y quitar de la cola. Al abrir un productor y un consumidor, se devuelven interfaces que contienen las API enqueue y dequeue.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Bucle principal**  
El uso de la cola se modela después del problema de productor/consumidor clásico. Piense en esto desde una perspectiva por dispositivo. Cada dispositivo debe realizar estos pasos: quitar de la cola para obtener una superficie de su cola de consumo, procesar en la superficie y, a continuación, poner en cola en su cola de producción. En el caso del dispositivo Direct3D 11, el uso de Direct3D 9 es casi idéntico.  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



**Limpieza**  
Este paso es muy sencillo. Además de los pasos normales para limpiar las API de Direct3D, la aplicación debe liberar las interfaces COM devueltas.  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a>Uso sin bloqueo

El ejemplo anterior tiene sentido para un caso de uso multiproceso en el que cada dispositivo tiene su propio subproceso. En el ejemplo se usan las versiones de bloqueo de las API: Infinite para el tiempo de espera y no hay ninguna marca para poner en cola. Si desea usar el ayudante sin bloqueos, solo tiene que realizar algunos cambios en el proceso. En esta sección se muestra el uso sin bloqueo con ambos dispositivos en un subproceso.

**Inicialización**  
La inicialización es idéntica salvo para las marcas. Dado que la aplicación es de un solo subproceso, use esa marca para crearla. Esto desactiva parte del código de sincronización, lo que puede mejorar el rendimiento.  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



La apertura de los dispositivos de productor y consumidor son las mismas que en el ejemplo de bloqueo.  
**Usar la cola**  
Hay muchas maneras de usar la cola en un modo de no bloqueo con diversas características de rendimiento. El siguiente ejemplo es sencillo, pero tiene un rendimiento deficiente debido al giro y el sondeo excesivos. A pesar de estos problemas, en el ejemplo se muestra cómo usar el ayudante. El enfoque consiste en permanecer constante en un bucle y quitar de la cola, procesar, poner en cola y vaciar. Si se produce un error en cualquiera de los pasos porque el recurso no está disponible, la aplicación simplemente vuelve a intentar el siguiente bucle.  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



Una solución más compleja podría comprobar el valor devuelto de enqueue y de Flush para determinar si es necesario el vaciado.  
</dl>

### <a name="three-devices"></a>Tres dispositivos

La extensión de los ejemplos anteriores para abarcar varios dispositivos es sencilla. En el código siguiente se realiza la inicialización. Una vez creados los objetos productor/consumidor, el código para usarlos es el mismo. Este ejemplo tiene tres dispositivos y, por tanto, tres colas. Las superficies fluyen de Direct3D 9 a Direct3D 10 a Direct3D 11.


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



Como se mencionó anteriormente, la clonación funciona de la misma manera, independientemente de la cola que se clona. Por ejemplo, la segunda llamada de clonación podría haber estado fuera del \_ objeto m 9to10Queue.


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a>Conclusión

Puede crear soluciones que usen la interoperabilidad para emplear la eficacia de varias API de DirectX. La interoperabilidad de la API de gráficos de Windows ahora ofrece un entorno de ejecución de Surface Management en Common 1,1. Este Runtime habilita la compatibilidad con el uso compartido de superficies sincronizadas dentro de las API recién desarrolladas, como Direct3D 11, Direct3D 10,1 y Direct2D. Mejoras de interoperabilidad entre nuevas API y API existentes ayuda a la migración de aplicaciones y compatibilidad con versiones anteriores. Las API de consumidor de Direct3D 9Ex y DXGI 1,1 pueden interoperar, como se muestra con el mecanismo de sincronización que se proporciona a través del código auxiliar de ejemplo en la galería de código de MSDN.

 

 
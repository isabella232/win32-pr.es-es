---
title: Uso compartido de superficie entre Windows API de gráficos
description: En este tema se proporciona información técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, incluidos Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a5d3e1b52691aeaee2373600dc247da679f0e452a6737741418e54df9490a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290231"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Uso compartido de superficie entre Windows API de gráficos

En este tema se proporciona información técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, incluidos Direct3D 11, Direct2D, DirectWrite, Direct3D 10 y Direct3D 9Ex. Si ya tiene conocimientos prácticos de estas API, este documento puede ayudarle a usar varias API para representarse en la misma superficie en una aplicación diseñada para los sistemas operativos Windows 7 o Windows Vista. En este tema también se proporcionan instrucciones de procedimientos recomendados y punteros a recursos adicionales.

> [!Note]  
> Para la interoperabilidad de Direct2D y DirectWrite en el entorno de ejecución de DirectX 11.1, puede usar [dispositivos Direct2D](/windows/desktop/Direct2D/devices-and-device-contexts) y contextos de dispositivo para representar directamente en dispositivos Direct3D 11.

 

En este tema se incluyen las siguientes secciones.

-   [Introducción](#introduction)
-   [Introducción a la interoperabilidad de API](#api-interoperability-overview)
-   [Escenarios de interoperabilidad](#interoperability-scenarios)
    -   [Uso compartido de dispositivos direct3D 10.1 con Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [Superficies compartidas sincronizadas de DXGI 1.1](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Conclusión](#conclusion)

## <a name="introduction"></a>Introducción

En este documento, Windows interoperabilidad de la API de gráficos hace referencia al uso compartido de la misma superficie de representación por diferentes API. Este tipo de interoperabilidad permite a las aplicaciones crear pantallas atractivas aprovechando varias API de gráficos Windows y facilitar la migración a nuevas tecnologías manteniendo la compatibilidad con las API existentes.

En Windows 7 (y Windows Vista SP2 con Windows 7 Interop Pack, Vista 7IP), las API de representación de gráficos son Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c y anteriores API de Direct3D, así como GDI y GDI+. Windows Imaging Component (WIC) y DirectWrite son tecnologías relacionadas para el procesamiento de imágenes, y Direct2D realiza la representación de texto. DirectX Video Acceleration API (DXVA), basada en Direct3D 9c y Direct3D 9Ex, se usa para el procesamiento de vídeo.

A Windows las API de gráficos evolucionan hacia la base de Direct3D, Microsoft invierte más esfuerzo en garantizar la interoperabilidad entre las API. Las API de Direct3D recién desarrolladas y las API de nivel superior basadas en las API de Direct3D también proporcionan compatibilidad cuando sea necesario para puentear la compatibilidad con api anteriores. Para ilustrar esto, las aplicaciones de Direct2D pueden usar Direct3D 10.1 mediante el uso compartido de un dispositivo Direct3D 10.1. Además, las API de Direct3D 11, Direct2D y Direct3D 10.1 pueden aprovechar las ventajas de Infraestructura de gráficos de DirectX (DXGI) 1.1, que permite superficies compartidas sincronizadas que admiten totalmente la interoperabilidad entre estas API. Las API basadas en DXGI 1.1 interoperan con GDI y con GDI+ por asociación, obteniendo el contexto de dispositivo GDI de una superficie DXGI 1.1. Para obtener más información, consulte la documentación de interoperabilidad de DXGI y GDI disponible en MSDN.

El tiempo de ejecución de Direct3D 9Ex admite el uso compartido de superficies no sincronizadas. Las aplicaciones de vídeo basadas en DXVA pueden usar el asistente de interoperabilidad Direct3D 9Ex y DXGI para la interoperabilidad de DXVA basada en Direct3D 9Ex con Direct3D 11 para el sombreador de proceso, o pueden interoperar con Direct2D para controles 2D o representación de texto. WIC y DirectWrite interoperan también con GDI, Direct2D y, por asociación, otras API de Direct3D.

Direct3D 10.0, Direct3D 9c y entornos de ejecución anteriores de Direct3D no admiten superficies compartidas. Las copias de memoria del sistema se seguirán usando para la interoperabilidad con las API basadas en GDI o DXGI.

Tenga en cuenta que los escenarios de interoperabilidad de este documento hacen referencia a varias API de gráficos que se representa en una superficie de representación compartida, en lugar de a la misma ventana de la aplicación. La sincronización de LAS API independientes que tienen como destino diferentes superficies que luego se composiciónn en la misma ventana está fuera del ámbito de este documento.

## <a name="api-interoperability-overview"></a>Introducción a la interoperabilidad de API

La interoperabilidad del uso compartido de superficie Windows api gráficas se puede describir en términos de escenarios de API a API y la funcionalidad de interoperabilidad correspondiente. A partir de Windows 7 y a partir de Windows Vista SP2 con 7IP, las nuevas API y los entornos de ejecución asociados incluyen Direct2D y tecnologías relacionadas: Direct3D 11 y DXGI 1.1. El rendimiento de GDI también se mejoró en Windows 7. Direct3D 10.1 se introdujo en Windows Vista SP1. En el diagrama siguiente se muestra la compatibilidad de interoperabilidad entre las API.

![diagrama de compatibilidad de interoperabilidad entre las API de gráficos de Windows](images/surface-sharing-interoperability.png)

En este diagrama, las flechas muestran escenarios de interoperabilidad en los que las API conectadas pueden acceder a la misma superficie. Las flechas azules indican mecanismos de interoperabilidad introducidos en Windows Vista. Las flechas verdes indican compatibilidad de interoperabilidad con nuevas API o mejoras que ayudan a las API anteriores a interoperar con api más recientes. Por ejemplo, las flechas verdes representan el uso compartido de dispositivos, la compatibilidad con la superficie compartida sincronizada, el asistente de sincronización de Direct3D 9Ex/DXGI y la obtención de un contexto de dispositivo GDI desde una superficie compatible.

## <a name="interoperability-scenarios"></a>Escenarios de interoperabilidad

A partir de Windows 7 y Windows Vista 7IP, las ofertas estándar de las API de gráficos de Windows admiten la representación de varias API en la misma superficie DXGI 1.1.

**Direct3D 11, Direct3D 10.1, Direct2D: interoperabilidad entre sí**

Las API de Direct3D 11, Direct3D 10.1 y Direct2D (y sus API relacionadas, como DirectWrite y WIC) pueden interoperar entre sí mediante el uso compartido de dispositivos direct3D 10.1 o superficies compartidas sincronizadas.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Uso compartido de dispositivos direct3D 10.1 con Direct2D

El uso compartido de dispositivos entre Direct2D y Direct3D 10.1 permite que una aplicación use ambas API para representar sin problemas y de forma eficaz en la misma superficie DXGI 1.1, con el mismo objeto de dispositivo Direct3D subyacente. Direct2D proporciona la capacidad de llamar a las API de Direct2D mediante un dispositivo Direct3D 10.1 existente, aprovechando el hecho de que Direct2D se basa en los entornos de ejecución de Direct3D 10.1 y DXGI 1.1. Los fragmentos de código siguientes muestran cómo Direct2D obtiene el destino de representación del dispositivo Direct3D 10.1 desde una superficie DXGI 1.1 asociada al dispositivo. El destino de representación del dispositivo Direct3D 10.1 puede ejecutar llamadas de dibujo de Direct2D entre las API BeginDraw y EndDraw.


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

-   El dispositivo Direct3D 10.1 asociado debe admitir el formato BGRA. Ese dispositivo se creó mediante una llamada a D3D10CreateDevice1 con el parámetro D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT. El formato BGRA se admite a partir del nivel de característica 9.1 de Direct3D 10.
-   La aplicación no debe crear varios ID2D1RenderTargets asociados al mismo dispositivo Direct3D10.1.
-   Para obtener un rendimiento óptimo, mantenga al menos un recurso alrededor en todo momento, como texturas o superficies asociadas al dispositivo.

El uso compartido de dispositivos es adecuado para el uso en proceso de un solo subproceso de un dispositivo de representación compartido por las API de representación de Direct3D 10.1 y Direct2D. Las superficies compartidas sincronizadas permiten el uso multiproceso, en proceso y fuera de proceso de varios dispositivos de representación que usan las API de Direct3D 10.1, Direct2D y Direct3D 11.

Otro método de interoperabilidad de Direct3D 10.1 y Direct2D es mediante ID3D1RenderTarget::CreateSharedBitmap, que crea un objeto ID2D1Bitmap a partir de IDXGISurface. Puede escribir una escena de Direct3D10.1 en el mapa de bits y representarla con Direct2D. Para obtener más información, [vea ID2D1RenderTarget::CreateSharedBitmap (Método).](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)

### <a name="direct2d-software-rasterization"></a>Rasterización de software de Direct2D

No se admite el uso compartido de dispositivos con Direct3D 10.1 cuando se usa el representador de software de Direct2D, por ejemplo, especificando D2D1 \_ RENDER TARGET USAGE FORCE SOFTWARE RENDERING en D2D1 RENDER TARGET USAGE al crear un destino de representación \_ \_ de \_ \_ \_ \_ \_ \_ Direct2D.

Direct2D puede usar el rasterizador de software WARP10 para compartir el dispositivo con Direct3D 10 o Direct3D 11, pero el rendimiento disminuye significativamente.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>Superficies compartidas sincronizadas de DXGI 1.1

Las API de Direct3D 11, Direct3D 10.1 y Direct2D usan DXGI 1.1, que proporciona la funcionalidad para sincronizar la lectura y escritura en la misma superficie de memoria de vídeo (DXGISurface1) mediante dos o más dispositivos Direct3D. Los dispositivos de representación que usan superficies compartidas sincronizadas pueden ser dispositivos Direct3D 10.1 o Direct3D 11, cada uno de los que se ejecutan en el mismo proceso o entre procesos.

Las aplicaciones pueden usar superficies compartidas sincronizadas para interoperar entre cualquier dispositivo basado en DXGI 1.1, como Direct3D 11 y Direct3D 10.1, o entre Direct3D 11 y Direct2D, mediante la obtención del dispositivo Direct3D 10.1 del objeto de destino de representación de Direct2D.

En direct3D 10.1 y las API posteriores, para usar DXGI 1.1, asegúrese de que el dispositivo Direct3D se crea mediante un objeto de adaptador DXGI 1.1, que se enumera desde el objeto de generador DXGI 1.1. Llame a CreateDXGIFactory1 para crear el objeto IDXGIFactory1 y EnumAdapters1 para enumerar el objeto IDXGIAdapter1. El objeto IDXGIAdapter1 debe pasarse como parte de la llamada D3D10CreateDevice o D3D10CreateDeviceAndSwapChain. Para obtener más información sobre las API de DXGI 1.1, consulte la Guía [de programación de DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>API existentes

**RECURSO D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**  
Al crear el recurso compartido sincronizado, establezca D3D10 \_ RESOURCE \_ MISC SHARED KEYEDMUTEX en LA MARCA MISC DEL RECURSO \_ \_ D3D10. \_ \_ \_  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**RECURSO D3D10 \_ \_ MISC \_ SHARED \_ KEYEDMUTEX**  
Permite sincronizar el recurso creado mediante las API IDXGIKeyedMutex::AcquireSync y ReleaseSync. Las siguientes API de direct3D 10.1 de creación de recursos que toman un parámetro MISC FLAG DE RECURSOS D3D10 se han ampliado para admitir la \_ \_ nueva \_ marca.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1::CreateBuffer

  
Si se llama a cualquiera de las funciones enumeradas con la marca MISC SHARED KEYEDMUTEX de D3D10 RESOURCE, se puede consultar la interfaz devuelta para una interfaz \_ \_ \_ IDXGIKeyedMutex, que implementa las API AcquireSync y ReleaseSync para sincronizar el acceso a la \_ superficie. El dispositivo que crea la superficie y cualquier otro dispositivo que abra la superficie (mediante OpenSharedResource) es necesario llamar a IDXGIKeyedMutex::AcquireSync antes de cualquier comando de representación en la superficie e IDXGIKeyedMutex::ReleaseSync cuando haya terminado de representarse.  
Los dispositivos WARP y REF no admiten recursos compartidos. Al intentar crear un recurso con esta marca en un dispositivo WARP o REF, el método create devolverá un código de \_ error E OUTOFMEMORY.  
**IDXGIKEYEDMUTEX (INTERFAZ)**  
Una nueva interfaz de DXGI 1.1, IDXGIKeyedMutex, representa una exclusión mutua con clave, que permite el acceso exclusivo a un recurso compartido que usan varios dispositivos. Para obtener documentación de referencia sobre esta interfaz y sus dos métodos, AcquireSync y ReleaseSync, vea [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Ejemplo: Uso compartido de surface sincronizado entre dos dispositivos Direct3D 10.1

En el ejemplo siguiente se muestra cómo compartir una superficie entre dos dispositivos Direct3D 10.1. La superficie compartida sincronizada se crea mediante un dispositivo Direct3D10.1.


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



El mismo dispositivo Direct3D10.1 puede obtener la superficie compartida sincronizada para su representación mediante una llamada a AcquireSync y, a continuación, liberar la superficie para la representación del otro dispositivo mediante una llamada a ReleaseSync. Cuando no se comparte la superficie compartida sincronizada con ningún otro dispositivo Direct3D, el creador puede obtener y liberar la superficie compartida sincronizada (para iniciar y finalizar la representación) adquiriendo y liberando con el mismo valor de clave.


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



El segundo dispositivo Direct3D10.1 puede obtener la superficie compartida sincronizada para su representación mediante una llamada a AcquireSync y, a continuación, liberar la superficie para la representación del primer dispositivo mediante una llamada a ReleaseSync. Tenga en cuenta que el dispositivo 2 puede adquirir la superficie compartida sincronizada con el mismo valor de clave que el especificado en la llamada ReleaseSync del dispositivo 1.


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



Los dispositivos adicionales que comparten la misma superficie pueden turnar la adquisición y liberación de la superficie mediante claves adicionales, como se muestra en las llamadas siguientes.


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



Tenga en cuenta que una aplicación real siempre podría representarse en una superficie intermedia que luego se copia en la superficie compartida para evitar que un dispositivo esté esperando en otro dispositivo que comparta la superficie.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Uso de superficies compartidas sincronizadas con Direct2D y Direct3D 11

Del mismo modo, para compartir entre las API de Direct3D 11 y Direct3D 10.1, se puede crear una superficie compartida sincronizada desde cualquier dispositivo de API y compartirla con los demás dispositivos de API, dentro o fuera de proceso.

Las aplicaciones que usan Direct2D pueden compartir un dispositivo Direct3D 10.1 y usar una superficie compartida sincronizada para interoperar con Direct3D 11 u otros dispositivos Direct3D 10.1, tanto si pertenecen al mismo proceso como a procesos diferentes. Sin embargo, para las aplicaciones de un solo proceso y subproceso, el uso compartido de dispositivos es el método de interoperabilidad más eficaz y de alto rendimiento entre Direct2D y Direct3D 10 o Direct3D 11.

### <a name="software-rasterizer"></a>Rasterizador de software

Las superficies compartidas sincronizadas no se admiten cuando las aplicaciones usan los rasterizadores de software Direct3D o Direct2D, incluidos el rasterizador de referencia y WARP, en lugar de usar la aceleración de hardware gráfico.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilidad entre las API basadas en Direct3D 9Ex y DXGI

Las API de Direct3D 9Ex incluían la noción de uso compartido de superficie para permitir que otras API leyesen desde la superficie compartida. Para compartir la lectura y escritura en una superficie compartida de Direct3D 9Ex, debe agregar la sincronización manual a la propia aplicación.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Superficies compartidas de Direct3D 9Ex más el asistente de sincronización manual

La tarea más fundamental en la interoperabilidad de Direct3D 9Ex y Direct3D 10 o 11 es pasar una sola superficie del primer dispositivo (dispositivo A) al segundo (dispositivo B), de modo que cuando el dispositivo B adquiere un identificador en la superficie, se garantiza que la representación del dispositivo A se ha completado. Por lo tanto, el dispositivo B puede usar esta superficie sin preocuparse. Esto es muy similar al problema clásico productor-consumidor y esta discusión modela el problema de esa manera. El primer dispositivo que usa la superficie y, a continuación, lo vuelve a hacer, es el productor (dispositivo A) y el dispositivo que está esperando inicialmente es el consumidor (dispositivo B). Cualquier aplicación real es más sofisticada que esta y encadenará varios bloques de creación productor-consumidor para crear la funcionalidad deseada.

Los bloques de creación productor-consumidor se implementan en el asistente mediante una cola de superficies. El productor coloca las superficies en cola y las quita el consumidor. El asistente presenta tres interfaces COM: ISurfaceQueue, ISurfaceProducer e ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>High-Level información general del asistente

El objeto ISurfaceQueue es el bloque de creación para usar las superficies compartidas. Se crea con un dispositivo Direct3D inicializado y una descripción para crear un número fijo de superficies compartidas. El objeto queue administra la creación de recursos y la apertura del código. El número y el tipo de superficies son fijos; Una vez creadas las superficies, la aplicación no puede agregarlas ni quitarlas.

Cada instancia del objeto ISurfaceQueue proporciona una clase de calle un solo sentido que se puede usar para enviar superficies desde el dispositivo de producción al dispositivo que lo consume. Se pueden usar varias calles unedadas para habilitar escenarios de uso compartido de superficie entre dispositivos de aplicaciones específicas.

**Creación/Duración de objetos**  
Hay dos maneras de crear el objeto de cola: a través de CreateSurfaceQueue o mediante el método Clone de ISurfaceQueue. Dado que las interfaces son objetos COM, se aplica la administración de la duración COM estándar.  
**Modelo productor/consumidor**  
Poner en cola (): el productor llama a esta función para indicar que se ha hecho con la superficie, que ahora puede estar disponible para otro dispositivo. Al volver de esta función, el dispositivo productor ya no tiene derechos sobre la superficie y no es seguro seguir usando esta función.  
Quitar la cola (): el dispositivo de consumo llama a esta función para obtener una superficie compartida. La API garantiza que las superficies quitadas de la cola están listas para usarse.  
**Metadata**  
La API admite la asociación de metadatos a las superficies compartidas.  
Enqueue() tiene la opción de especificar metadatos adicionales que se pasarán al dispositivo de consumo. Los metadatos deben ser menores que un máximo conocido en el momento de la creación.  
Dequeue() puede pasar opcionalmente un búfer y un puntero al tamaño del búfer. La cola rellena el búfer con los metadatos de la llamada a Enqueue correspondiente.  
**Clonación**  
Cada objeto ISurfaceQueue resuelve una sincronización un solo sentido. Se supone que la gran mayoría de las aplicaciones que usan esta API usarán un sistema cerrado. El sistema cerrado más sencillo con dos dispositivos que envían superficies de un lado a otro requiere dos colas. El objeto ISurfaceQueue tiene un método Clone() para que sea posible crear varias colas que forman parte de la misma canalización de mayor tamaño.  
Clone crea un nuevo objeto ISurfaceQueue a partir de uno existente y comparte todos los recursos abiertos entre ellos. El objeto resultante tiene exactamente las mismas superficies que la cola de origen. Las colas clonadas pueden tener tamaños de metadatos diferentes entre sí.  
**Superficies**  
ISurfaceQueue asume la responsabilidad de crear y administrar sus superficies. No es válido poner en cola superficies arbitrarias. Además, una superficie solo debe tener un "propietario" activo. Debe estar en una cola específica o ser utilizada por un dispositivo específico. No es válido tenerla en varias colas o para que los dispositivos sigan usando la superficie después de ponerla en cola.  
</dl>

### <a name="api-details"></a>Detalles de la API

### <a name="isurfacequeue"></a>IsurfaceQueue

La cola es responsable de crear y mantener los recursos compartidos. También proporciona la funcionalidad para encadenar varias colas mediante Clonar. La cola tiene métodos que abren el dispositivo de producción y un dispositivo de consumo. Solo se puede abrir una de ellas en cualquier momento.

La cola expone las siguientes API:



| API                            | Descripción                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Crea un objeto ISurfaceQueue (la cola "raíz").                              |
| ISurfaceQueue::OpenConsumer | Devuelve una interfaz para que el dispositivo de consumo se descola.                        |
| ISurfaceQueue::OpenProducer | Devuelve una interfaz para que el dispositivo de producción se poner en cola.                        |
| ISurfaceQueue::Clone        | Crea un objeto ISurfaceQueue que comparte superficies con el objeto de cola raíz. |



 

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

**Width**, **Height**  Las dimensiones de las superficies compartidas. Todas las superficies compartidas deben tener las mismas dimensiones.  
**Formato** Formato de las superficies compartidas. Todas las superficies compartidas deben tener el mismo formato. Los formatos válidos dependen de los dispositivos que se usarán, ya que diferentes pares de dispositivos pueden compartir diferentes tipos de formato.  
**NumSurfaces**  Número de superficies que forman parte de la cola. Se trata de un número fijo.  
 **MetaDataSize**  Tamaño máximo del búfer de metadatos.  
**Marcas**  Marcas para controlar el comportamiento de la cola. Vea la sección Comentarios.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parámetros**

 *pDesc* \[ en \]  La descripción de la cola de superficie compartida que se va a crear.  

 *pDevice* \[ en \]  El dispositivo que se debe usar para crear las superficies compartidas. Se trata de un parámetro explícito debido a una característica de Windows Vista. Para las superficies compartidas entre Direct3D 9 y Direct3D 10, las superficies deben crearse con Direct3D 9.  

 *ppQueue* \[ out \]  En la devolución, contiene un puntero al objeto ISurfaceQueue.  


**Valores devueltos**

Si *pDevice* no es capaz de compartir recursos, esta función devuelve DXGI \_ ERROR INVALID \_ \_ CALL. Esta función crea los recursos. Si se produce un error, devuelve un error. Si se realiza correctamente, devuelve S \_ OK.

**Comentarios:**

Al crear el objeto queue también se crean todas las superficies. Se supone que todas las superficies son destinos de representación 2D y se crearán con las marcas D3D10 BIND RENDER TARGET y \_ \_ \_ D3D10 \_ BIND SHADER RESOURCE \_ \_ establecidas (o las marcas equivalentes para los distintos tiempos de ejecución).

El desarrollador puede especificar una marca que indica si varios subprocesos accederán a la cola. Si no se establece ninguna marca ( Flags == 0), varios **subprocesos** usarán la cola. El desarrollador puede especificar el acceso de subproceso único, lo que desactiva el código de sincronización y proporciona una mejora del rendimiento para esos casos. Cada cola clonada tiene su propia marca, por lo que es posible que las distintas colas del sistema tengan controles de sincronización diferentes.

 **Abrir un productor**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parámetros**  

*pDevice* \[ En\]  

El dispositivo productor que pone en cola las superficies en la cola de superficie. 

*ppProducer* \[ out \] Devuelve un objeto a la interfaz del productor.  


**Valores devueltos**

Si el dispositivo no es capaz de compartir superficies, devuelve DXGI \_ ERROR \_ INVALID \_ CALL.

**Abrir un consumidor**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parámetros**  
 *pDevice* \[ En\]  
 El dispositivo consumidor que quita las superficies de la cola de superficie. 
 *ppConsumer* \[ out \]  Devuelve un objeto a la interfaz de consumidor.  


**Valores devueltos**

Si el dispositivo no es capaz de compartir superficies, devuelve DXGI \_ ERROR \_ INVALID \_ CALL.

**Comentarios:**

Esta función abre todas las superficies de la cola para el dispositivo de entrada y las almacena en caché. Las llamadas posteriores a Dequeue simplemente irán a la memoria caché y no tendrán que volver a abrir las superficies cada vez.



### <a name="cloning-an-idxgixsurfacequeue"></a>Clonación de IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



**Los** **miembros MetaDataSize** **y Flags** tienen el mismo comportamiento que para CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parámetros**

*pDesc* \[ en \] un struct que proporciona una descripción del objeto Clone que se va a crear. Este parámetro se debe inicializar.  
*ppQueue* \[ out \] Devuelve el objeto inicializado.  
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
*id* \[ en\]  
EL REFIID de una superficie 2D del dispositivo que lo consume.  

-   Para un IDirect3DDevice9, el REFIID debe ser \_ \_ uuidof(IDirect3DTexture9).
-   Para un id3D10Device, el REFIID debe ser \_ \_ uuidof(ID3D10Texture2D).
-   Para un id3D11Device, el REFIID debe ser \_ \_ uuidof(ID3D11Texture2D).

*ppSurface* \[ out \] Devuelve un puntero a la superficie.  
*pBuffer* \[ in, out Un parámetro opcional y, si no es NULL, en la devolución, contiene los metadatos que se pasaron en la \] llamada de puesta en cola correspondiente.   
*pBufferSize* \[ in, out \] El tamaño de *pBuffer*, en bytes. Devuelve el número de bytes devueltos en *pBuffer.* Si la llamada de puesta en cola no proporciona metadatos, *pBuffer* se establece en 0.  
*dwTimeout* \[ en \] Especifica un valor de tiempo de espera. Consulte los comentarios para obtener más detalles.  
</dl>

**Valores devueltos**

Esta función puede devolver WAIT TIMEOUT si se especifica un valor de tiempo de espera y la función \_ no devuelve antes del valor de tiempo de espera. Vea la sección Comentarios. Si no hay ninguna superficie disponible, la función devuelve con *ppSurface* establecido en **NULL,** *pBufferSize* establecido en 0 y el valor devuelto es 0x80070120 (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)).  
</dl>

**Comentarios:**

Esta API puede bloquearse si la cola está vacía. El *parámetro dwTimeout* funciona de forma idéntica a Windows API de sincronización, como WaitForSingleObject. Para el comportamiento de no bloqueo, use un tiempo de espera de 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Esta interfaz proporciona dos métodos que permiten a la aplicación poner en cola superficies. Una vez puesta en cola una superficie, el puntero de superficie ya no es válido y no es seguro de usar. La única acción que la aplicación debe realizar con el puntero es liberarla.



| Método                          | Descripción                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer::Enqueue | Pone en cola una superficie en el objeto de cola. Una vez completada esta llamada, el productor se realiza con la superficie y la superficie está lista para otro dispositivo. |
| ISurfaceProducer::Flush   | Se usa si las aplicaciones deben tener un comportamiento sin bloqueo. Para obtener información detallada, vea la sección Comentarios de.                                                                  |



 

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
*pSurface* \[ En\]  
Superficie del dispositivo de producción que se debe poner en cola. Esta superficie debe ser una superficie quitada de la cola de la misma red de cola. *pBuffer* \[ en \] Un parámetro opcional, que se usa para pasar metadatos. Debe apuntar a los datos que se pasarán a la llamada de eliminación de cola.  
*BufferSize* \[ en \] El tamaño de *pBuffer*, en bytes.  
*Marcas* \[ en \] Un parámetro opcional que controla el comportamiento de esta función. La única marca es SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT. Consulte los comentarios de Flush. Si no se pasa ninguna marca (*Flags* == 0), se usa el comportamiento de bloqueo predeterminado.  
</dl>

**Valores devueltos**

Esta función puede devolver DXGI ERROR WAS STILL DRAWING si se usa una marca \_ SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT.  
</dl>

**Comentarios:**

-   Esta función coloca la superficie en la cola. Si la aplicación no especifica SURFACE QUEUE FLAG DO NOT WAIT, esta función está bloqueando y realizará una sincronización de \_ \_ \_ \_ GPU-CPU para garantizar que toda la representación en la superficie puesta en cola está \_ completa. Si esta función se realiza correctamente, habrá una superficie disponible para la eliminación de la cola. Si desea un comportamiento sin bloqueo, use la \_ marca NO \_ ESPERAR. Consulte Flush() para obtener más información.
-   Según las reglas de recuento de referencias COM, la superficie devuelta por Dequeue será AddRef(), por lo que la aplicación no necesita hacerlo. Después de llamar a Enqueue, la aplicación debe liberar la superficie porque ya no la usa.

**Vaciar**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parámetros**  
*Marcas* \[ En\]  
La única marca es SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT. Vea la sección Comentarios. *nSurfaces* \[ out \] Devuelve el número de superficies que todavía están pendientes y no vacías.  
</dl>

**Valores devueltos**

Esta función puede devolver DXGI ERROR WAS STILL DRAWING si se usa la marca \_ SURFACE QUEUE FLAG DO \_ NOT \_ \_ \_ \_ \_ \_ \_ WAIT. Esta función devuelve S OK si alguna superficie se ha vaciado \_ correctamente. Esta función devuelve DXGI \_ ERROR WAS STILL DRAWING solo si no se ha vaciado ninguna \_ \_ \_ superficie. Juntos, el valor devuelto y *nSurfaces* indican a la aplicación qué trabajo se ha realizado y si queda algún trabajo por hacer.  
</dl>

**Comentarios:**

El vaciado solo es significativo si la llamada anterior a enqueue usó la marca DO NOT WAIT; de \_ \_ lo contrario, será una operación no op. Si la llamada a enqueue usa la marca DO NOT WAIT, la puesta en cola se devuelve inmediatamente y no se garantiza la sincronización \_ \_ de GPU-CPU. La superficie todavía se considera puesta en cola, el dispositivo de producción no puede seguir usándose, pero no está disponible para la eliminación de la cola. Para intentar confirmar la superficie para la eliminación de la cola, se debe llamar a Flush. El vaciado intenta confirmar todas las superficies que están actualmente en cola. Si no se pasa ninguna marca a Flush, bloqueará y borrará toda la cola y preparará todas las superficies de ella para su eliminación de la cola. Si se usa la marca NO ESPERAR, la cola comprobará las superficies para ver si alguna de ellas está lista; este paso no \_ \_ es de bloqueo. Las superficies que han finalizado la sincronización gpu-CPU estarán listas para el dispositivo consumidor. Las superficies que aún están pendientes no se verán afectadas. La función devuelve el número de superficies que todavía deben vaciarse.

> [!Note]  
> El vaciado no interrumpirá la semántica de la cola. La API garantiza que las superficies puestas en cola primero se confirman antes de que las superficies se pondrán en cola más adelante, independientemente de cuándo se produce la sincronización de GPU-CPU.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Asistente de interoperabilidad de Direct3D 9Ex y DXGI: Cómo usar

Esperamos que la mayoría de los casos de uso impliquen dos dispositivos que comparten varias superficies. Dado que este también es el escenario más sencillo, en este documento se detalla cómo usar las API para lograr este objetivo, se describe una variación sin bloqueo y finaliza con una breve sección sobre la inicialización de tres dispositivos.

### <a name="two-devices"></a>Dos dispositivos

La aplicación de ejemplo que usa este asistente puede usar Direct3D 9Ex y Direct3D 11 juntos. La aplicación puede procesar contenido con ambos dispositivos y presentar contenido mediante Direct3D 9. El procesamiento podría significar la representación de contenido, la decodificación de vídeo, la ejecución de sombreadores de proceso, y así sucesivamente. Para cada fotograma, la aplicación primero se procesará con Direct3D 11, luego se procesará con Direct3D 9 y, por último, se presentará con Direct3D 9. Además, el procesamiento con Direct3D 11 producirá algunos metadatos que direct3D 9 presente tendrá que consumir. En esta sección se trata el uso del asistente en tres partes que corresponden a esta secuencia: Inicialización, Bucle principal y Limpieza.

**Inicialización**  
La inicialización implica los pasos siguientes:  

1.  Inicialice ambos dispositivos.
2.  Cree la cola raíz: m \_ 11to9Queue.
3.  Clone desde la cola raíz: m \_ 9to11Queue.
4.  Llame a OpenProducer/OpenConsumer en ambas colas.

Los nombres de cola usan los números 9 y 11 para indicar qué API es el productor y cuál es el consumidor: **m \_**_producer_*_to_*_consumer_*_Queue_*. En consecuencia, m 11to9Queue indica una cola para la que el dispositivo Direct3D 11 genera superficies que el dispositivo \_ Direct3D 9 consume. De forma similar, m 9to11Queue indica una cola para la que \_ Direct3D 9 genera superficies que consume Direct3D 11.  
La cola raíz está inicialmente llena y todas las colas clonadas están inicialmente vacías. Esto no debería ser un problema para la aplicación, excepto para el primer ciclo de puestas en cola y eliminaciones de colas y la disponibilidad de los metadatos. Si una cola solicita metadatos pero no se estableció ninguno (ya sea porque no hay nada inicialmente o la cola no estableció nada), la eliminación de la cola ve que no se ha recibido ningún metadato.  

1.  **Inicialice ambos dispositivos.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Cree la cola raíz.**  
    Este paso también crea las superficies. Las restricciones de tamaño y formato son idénticas a la creación de cualquier recurso compartido. El tamaño del búfer de metadatos se fija en el momento de la creación y, en este caso, solo pasaremos un UINT.  
    La cola debe crearse con un número fijo de superficies. El rendimiento variará en función del escenario. Tener varias superficies aumenta las posibilidades de que los dispositivos estén ocupados. Por ejemplo, si solo hay una superficie, no habrá paralelización entre los dos dispositivos. Por otro lado, aumentar el número de superficies aumenta la superficie de memoria, lo que puede degradar el rendimiento. En este ejemplo se usan dos superficies.  
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
    Cada cola clonada debe usar las mismas superficies, pero puede tener diferentes tamaños de búfer de metadatos y marcas diferentes. En este caso, no hay metadatos de Direct3D 9 a Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Abra los dispositivos productor y consumidor.**  
    La aplicación debe realizar este paso antes de llamar a Enqueue y Dequeue. Al abrir un productor y un consumidor, se devuelven interfaces que contienen las API de puesta en cola o eliminación de la cola.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Bucle main**  
El uso de la cola se modela después del problema clásico entre productor y consumidor. Piense en esto desde una perspectiva por dispositivo. Cada dispositivo debe realizar estos pasos: quitar la cola para obtener una superficie de su cola de consumo, procesarla en la superficie y, a continuación, ponerla en cola en la cola de producción. Para el dispositivo Direct3D 11, el uso de Direct3D 9 es casi idéntico.  


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
Este paso es muy sencillo. Además de los pasos normales para limpiar las API de Direct3D, la aplicación debe liberar las interfaces COM de retorno.  


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

El ejemplo anterior tiene sentido para un caso de uso multiproceso en el que cada dispositivo tiene su propio subproceso. En el ejemplo se usan las versiones de bloqueo de las API: INFINITE para el tiempo de espera y ninguna marca para poner en cola. Si desea usar el asistente de una manera sin bloqueo, solo tiene que realizar algunos cambios. En esta sección se muestra el uso sin bloqueo con ambos dispositivos en un subproceso.

**Inicialización**  
La inicialización es idéntica, excepto para las marcas . Dado que la aplicación es de un solo subproceso, use esa marca para la creación. Esto desactiva parte del código de sincronización, lo que potencialmente mejora el rendimiento.  


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



La apertura de los dispositivos de productor y consumidor es la misma que en el ejemplo de bloqueo.  
**Uso de la cola**  
Hay muchas maneras de usar la cola de forma sin bloqueo con varias características de rendimiento. El ejemplo siguiente es sencillo, pero tiene un rendimiento deficiente debido a un giro y sondeo excesivos. A pesar de estos problemas, en el ejemplo se muestra cómo usar el asistente. El enfoque es colocarse constantemente en un bucle y quitar la cola, procesar, poner en cola y vaciar. Si alguno de los pasos genera un error porque el recurso no está disponible, la aplicación simplemente intenta de nuevo el bucle siguiente.  


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



Una solución más compleja podría comprobar el valor devuelto de puesta en cola y de vaciado para determinar si es necesario vaciar.  
</dl>

### <a name="three-devices"></a>Tres dispositivos

Ampliar los ejemplos anteriores para abarcar varios dispositivos es sencillo. El código siguiente realiza la inicialización. Una vez creados los objetos Producer/Consumer, el código para usarlos es el mismo. Este ejemplo tiene tres dispositivos y, por tanto, tres colas. Las superficies fluyen de Direct3D 9 a Direct3D 10 a Direct3D 11.


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



Como se mencionó anteriormente, la clonación funciona de la misma manera, independientemente de la cola que se clone. Por ejemplo, la segunda llamada a Clone podría haber estado fuera del objeto m \_ 9to10Queue.


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

Puede crear soluciones que usen interoperabilidad para emplear la potencia de varias API de DirectX. Windows interoperabilidad de la API de gráficos ahora ofrece un entorno de ejecución común de administración de superficie DXGI 1.1. Este entorno de ejecución habilita la compatibilidad con el uso compartido de superficie sincronizada en las API recién desarrolladas, como Direct3D 11, Direct3D 10.1 y Direct2D. Las mejoras de interoperabilidad entre las nuevas API y las API existentes ayudan a la migración de aplicaciones y a la compatibilidad con versiones anteriores. Las API de consumidor de Direct3D 9Ex y DXGI 1.1 pueden interoperar, como se muestra con el mecanismo de sincronización proporcionado a través del código auxiliar de ejemplo en msdn code gallery.

 

 
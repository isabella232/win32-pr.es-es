---
title: Efectos personalizados
description: Muestra cómo escribir sus propios efectos personalizados mediante HLSL estándar.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149600"
---
# <a name="custom-effects"></a>Efectos personalizados

[Direct2D](./direct2d-portal.md) se suministra con una biblioteca de efectos que realizan una serie de operaciones de imagen comunes. Vea el tema sobre [efectos integrados](built-in-effects.md) para obtener una lista completa de los efectos. En el caso de las funciones que no se pueden lograr con los efectos integrados, Direct2D le permite escribir sus propios efectos personalizados mediante [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)estándar. Puede usar estos efectos personalizados junto con los efectos integrados que se envían con Direct2D.

Para ver ejemplos de un efecto completo de píxeles, vértices y sombreador de cálculo, consulte el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

En este tema, le mostraremos los pasos y los conceptos que necesita para diseñar y crear un efecto personalizado con todas las características.

## <a name="introduction-what-is-inside-an-effect"></a>Introducción: ¿Qué hay dentro de un efecto?

![diagrama de efecto de sombra paralela.](images/custom-effects1.png)

Conceptualmente, un efecto de [Direct2D](./direct2d-portal.md) realiza una tarea de creación de imágenes, como cambiar el brillo, dessaturar una imagen o como se mostró anteriormente, creando una sombra paralela. En la aplicación, son sencillas. Pueden aceptar cero o más imágenes de entrada, exponer varias propiedades que controlan su funcionamiento y generar una sola imagen de salida.

Hay cuatro partes diferentes de un efecto personalizado que el autor de un efecto es responsable de:

1.  Interfaz de efecto: la interfaz de efecto define conceptualmente cómo interactúa una aplicación con un efecto personalizado (como cuántas entradas acepta el efecto y qué propiedades están disponibles). La interfaz de efecto administra un gráfico de transformación, que contiene las operaciones de creación de imágenes reales.
2.  Transformar gráfico: cada efecto crea un gráfico de transformación interno formado por transformaciones individuales. Cada transformación representa una operación de una sola imagen. El efecto es responsable de vincular estas transformaciones en un gráfico para realizar el efecto de imagen previsto. Un efecto puede Agregar, quitar, modificar y reordenar las transformaciones en respuesta a los cambios en las propiedades externas del efecto.
3.  Transform: una transformación representa una operación de una sola imagen. Su finalidad principal es hospedar los sombreadores que se ejecutan para cada píxel de salida. Para ello, es responsable de calcular el nuevo tamaño de la imagen de salida basándose en la lógica de sus sombreadores. También debe calcular qué área de la imagen de entrada deben leer los sombreadores para representar la región de salida solicitada.
4.  Sombreador: se ejecuta un sombreador en la entrada de la transformación en la GPU (o CPU si se especifica la representación de software cuando la aplicación crea el dispositivo Direct3D). Los sombreadores de efectos se escriben en el lenguaje de sombreado de alto nivel ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) y se compilan en código de bytes durante la compilación del efecto, que después se carga por el efecto durante el tiempo de ejecución. En este documento de referencia se describe cómo escribir HLSL compatible con [Direct2D](./direct2d-portal.md). La documentación de Direct3D contiene información general básica de HLSL.

## <a name="creating-an-effect-interface"></a>Crear una interfaz de efecto

La interfaz de efecto define cómo interactúa una aplicación con el efecto personalizado. Para crear una interfaz de efecto, una clase debe implementar ID2D1EffectImpl, definir metadatos que describan el efecto (como su nombre, recuento de entradas y propiedades) y crear métodos que registren el efecto personalizado para su uso con [Direct2D](./direct2d-portal.md).

Una vez que se han implementado todos los componentes de una interfaz de efecto, el encabezado de la clase se parecerá a este:


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a>Implementación de ID2D1EffectImpl

La interfaz [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contiene tres métodos que debe implementar:

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a>Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) llama al método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) una vez que la aplicación ha llamado al método [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) . Puede utilizar este método para realizar la inicialización interna o cualquier otra operación necesaria para el efecto. Además, puede utilizarlo para crear el gráfico de transformación inicial del efecto.

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a>SetGraph (ID2D1TransformGraph \* pTransformGraph)

[Direct2D](./direct2d-portal.md) llama al método [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) cuando se cambia el número de entradas del efecto. Aunque la mayoría de los efectos tienen un número constante de entradas, otras como el [efecto compuesto](composite.md) admiten un número variable de entradas. Este método permite que estos efectos actualicen su gráfico de transformación en respuesta a un recuento de entrada cambiante. Si un efecto no admite un recuento de entrada variable, este método simplemente puede devolver E \_ NOTIMPL.

### <a name="prepareforrender-d2d1_change_type-changetype"></a>PrepareForRender (tipo de cambio de D2D1 \_ \_ )

El método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) proporciona una oportunidad para que los efectos realicen operaciones en respuesta a cambios externos. [Direct2D](./direct2d-portal.md) llama a este método justo antes de representar un efecto si al menos uno de ellos es true:

-   El efecto se ha inicializado anteriormente, pero aún no se ha dibujado.
-   Una propiedad de efecto ha cambiado desde la última llamada a Draw.
-   El estado del contexto de [Direct2D](./direct2d-portal.md) que realiza la llamada (como dpi) ha cambiado desde la última llamada a Draw.

### <a name="implement-the-effect-registration-and-callback-methods"></a>Implementar los métodos de registro y devolución de llamada de efecto

Las aplicaciones deben registrar efectos con [Direct2D](./direct2d-portal.md) antes de crear una instancia de ellos. Este registro está en el ámbito de una instancia de un generador de Direct2D y debe repetirse cada vez que se ejecuta la aplicación. Para habilitar este registro, un efecto personalizado define un GUID único, un método público que registra el efecto y un método de devolución de llamada privado que devuelve una instancia del efecto.

### <a name="define-a-guid"></a>Definir un GUID

Debe definir un GUID que identifique de forma única el efecto de registro con [Direct2D](./direct2d-portal.md). La aplicación usa el mismo para identificar el efecto cuando llama a [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).

Este código muestra cómo definir dicho GUID para un efecto. Debe crear su propio GUID único mediante una herramienta de generación de GUID como guidgen.exe.


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a>Definir un método de registro público

A continuación, defina un método público para que la aplicación llame a para registrar el efecto con [Direct2D](./direct2d-portal.md). Dado que el registro de efectos es específico de una instancia de un generador de Direct2D, el método acepta una interfaz [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) como parámetro. Para registrar el efecto, el método llama entonces a la API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) en el parámetro **ID2D1Factory1** .

Esta API acepta una cadena XML que describe los metadatos, las entradas y las propiedades del efecto. Los metadatos de un efecto solo tienen fines informativos y la aplicación puede consultarlos a través de la interfaz [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) . Los datos de entrada y de propiedad, por otro lado, se usan en [Direct2D](./direct2d-portal.md) y representan la funcionalidad del efecto.

Aquí se muestra una cadena XML para un efecto de muestra mínimo. La adición de propiedades personalizadas al XML se trata en la sección agregar propiedades personalizadas a un efecto.


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a>Definir un método de devolución de llamada del generador de efectos

El efecto también debe proporcionar un método de devolución de llamada privado que devuelva una instancia del efecto a través de un único \* \* parámetro IUnknown. Se proporciona un puntero a este método a [Direct2D](./direct2d-portal.md) cuando el efecto se registra a través de la API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) a través del parámetro de [**\_ \_ generador de efectos PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a>Implementar la interfaz IUnknown

Por último, el efecto debe implementar la interfaz IUnknown para la compatibilidad con COM.

## <a name="creating-the-effects-transform-graph"></a>Crear el gráfico de transformación del efecto

Un efecto puede usar varias transformaciones diferentes (operaciones de imagen individuales) para crear el efecto de imagen deseado. Para controlar el orden en el que estas transformaciones se aplican a la imagen de entrada, el efecto las organiza en un gráfico de transformación. Un gráfico de transformación puede hacer uso de los efectos y las transformaciones incluidos en [Direct2D](./direct2d-portal.md) , así como las transformaciones personalizadas creadas por el autor del efecto.

### <a name="using-transforms-included-with-direct2d"></a>Usar transformaciones incluidas con Direct2D

Estas son las transformaciones que se usan con más frecuencia y que se proporcionan con [Direct2D](./direct2d-portal.md).

-   [**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): esta transformación combina un número arbitrario de entradas en función de una descripción de Blend, vea el tema de [**\_ \_ Descripción de D2D1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) y el [ejemplo de modos de efecto compuesto de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) para obtener ejemplos de fusión. Esta transformación es devuelta por el método [**ID2D1EffectContext:: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .
-   [**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): esta transformación expande el tamaño de salida de una imagen según el [**\_ \_ modo de extensión D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) especificado. Esta transformación es devuelta por el método [**ID2D1EffectContext:: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .
-   [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): esta transformación desplaza (traduce) su entrada en cualquier número entero de píxeles. Esta transformación es devuelta por el método [**ID2D1EffectContext:: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .
-   Cualquier efecto existente se puede tratar como una transformación con el fin de transformar la creación del gráfico mediante el método [**ID2D1EffectContext:: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .

### <a name="creating-a-single-node-transform-graph"></a>Crear un gráfico de transformación de un solo nodo

Una vez que se crea una transformación, la entrada del efecto debe estar conectada a la entrada de la transformación y la salida de la transformación debe estar conectada a la salida del efecto. Cuando un efecto solo contiene una única transformación, puede usar el método [**ID2D1TransformGraph:: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) para lograrlo fácilmente.

Puede crear o modificar una transformación en los métodos [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) o [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) del efecto mediante el parámetro ID2D1TransformGraph proporcionado. Si un efecto tiene que realizar cambios en el gráfico de transformación en otro método en el que este parámetro no está disponible, el efecto puede guardar el parámetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) como una variable miembro de la clase y acceder a él en otro lugar, como [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) o un método de devolución de llamada de propiedad personalizada.

Aquí se muestra un método de [**inicialización**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) de ejemplo. Este método crea un gráfico de transformación de un solo nodo que desplaza la imagen en 100 píxeles en cada eje.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a>Crear un gráfico de transformación de varios nodos

Agregar varias transformaciones al gráfico de transformación de un efecto permite que los efectos realicen internamente varias operaciones de imagen que se presentan a una aplicación como un solo efecto unificado.

Como se indicó anteriormente, el gráfico de transformación del efecto se puede editar en cualquier método de efecto mediante el parámetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) recibido en el método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) del efecto. Las siguientes API de esa interfaz se pueden usar para crear o modificar un gráfico de transformación de un efecto:

### <a name="addnodeid2d1transformnode-pnode"></a>AddNode (ID2D1TransformNode \* pNode)

El método [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , en efecto, ' registra ' la transformación con el efecto y se debe llamar antes de que se pueda usar la transformación con cualquiera de los demás métodos del gráfico de transformación.

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a>ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UINT32 toNodeInputIndex)

El método [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) conecta la entrada de imagen del efecto a la entrada de una transformación. La misma entrada de efecto puede estar conectada a varias transformaciones.

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a>ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UINT32 toNodeInputIndex)

El método [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) conecta la salida de una transformación a otra entrada de la transformación. Una salida de transformación se puede conectar a varias transformaciones.

### <a name="setoutputnodeid2d1transformnode-pnode"></a>SetOutputNode (ID2D1TransformNode \* pNode)

El método [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) conecta la salida de una transformación a la salida del efecto. Dado que un efecto solo tiene una salida, solo se puede designar una única transformación como el "nodo de salida".

Este código usa dos transformaciones independientes para crear un efecto unificado. En este caso, el efecto es una sombra paralela traducida.


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a>Agregar propiedades personalizadas a un efecto

Los efectos pueden definir propiedades personalizadas que permiten a una aplicación cambiar el comportamiento del efecto durante el tiempo de ejecución. Hay tres pasos para definir una propiedad para un efecto personalizado:

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a>Agregar los metadatos de la propiedad a los datos de registro del efecto

### <a name="add-property-to-registration-xml"></a>Agregar propiedad a XML de registro

Debe definir las propiedades de un efecto personalizado durante el registro inicial del efecto en [Direct2D](./direct2d-portal.md). En primer lugar, debe actualizar el XML de registro del efecto en su método de registro público con la nueva propiedad:


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



Cuando se define una propiedad de efecto en XML, se necesita un nombre, un tipo y un nombre para mostrar. El nombre para mostrar de una propiedad, así como los valores de categoría, autor y descripción del efecto general, pueden y deben localizarse.

Para cada propiedad, un efecto puede especificar opcionalmente valores predeterminados, mínimos y máximos. Estos valores son solo para uso informativo. No se aplican en [Direct2D](./direct2d-portal.md). Depende de usted implementar la lógica predeterminada/Min/Max especificada en la clase Effect.

El valor de tipo que aparece en el XML de la propiedad debe coincidir con el tipo de datos correspondiente utilizado por los métodos de captador y establecedor de la propiedad. En esta tabla se muestran los valores XML correspondientes para cada tipo de datos:



| Tipo de datos                                                                                                                              | Valor XML correspondiente |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| PWSTR                                                                                                                                  | string                  |
| BOOL                                                                                                                                   | bool                    |
| UINT                                                                                                                                   | uint32                  |
| INT                                                                                                                                    | int32                   |
| FLOAT                                                                                                                                  | FLOAT                   |
| [**\_Vector D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | vector2                 |
| [**\_Vector D2D \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | Vector3                 |
| [**D2D \_ Vector \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | Vector4                 |
| [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool)) | matrix3x2               |
| [**D2D \_ Matrix \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | matrix4x3               |
| [**\_Matriz D2D \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | matrix4x4               |
| [**D2D \_ Matrix \_ 5x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | matrix5x4               |
| BYTES\[\]                                                                                                                               | blob                    |
| IUnknown\*                                                                                                                             | IUnknown                |
| [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*                                                                                       | colorcontext            |
| CLSID                                                                                                                                  | clsid                   |
| Enumeración [**( \_ \_ modo de interpolación D2D1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)                                                | enum                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a>Asignar la nueva propiedad a métodos getter y Setter

A continuación, el efecto debe asignar esta nueva propiedad a los métodos getter y Setter. Esto se hace a través de la matriz de [**\_ \_ enlace de la propiedad D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) que se pasa al método [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .

La matriz de [**\_ \_ enlace de la propiedad D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) tiene el siguiente aspecto:


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



Una vez que cree la matriz XML y los enlaces, pásela al método [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



La \_ macro de enlace de tipo de valor D2D1 \_ \_ requiere que la clase de efecto herede de [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) antes que cualquier otra interfaz.

Las propiedades personalizadas de un efecto se indizan en el orden en el que se declaran en el XML y, una vez creada, la aplicación puede acceder a ella mediante los métodos [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) y [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) . Para mayor comodidad, puede crear una enumeración pública que muestre cada propiedad en el archivo de encabezado del efecto:


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a>Crear los métodos de captador y establecedor para la propiedad

El siguiente paso consiste en crear los métodos de captador y establecedor para la nueva propiedad. Los nombres de los métodos deben coincidir con los especificados en la matriz de [**\_ \_ enlace de la propiedad D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) . Además, el tipo de propiedad especificado en el XML del efecto debe coincidir con el tipo del parámetro del método setter y el valor devuelto del método del captador.


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a>Transformaciones del efecto de actualización en respuesta al cambio de propiedad

Para actualizar realmente la salida de la imagen de un efecto en respuesta a un cambio de propiedad, el efecto debe cambiar sus transformaciones subyacentes. Esto se hace normalmente en el método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) del efecto, al que [Direct2D](./direct2d-portal.md) llama automáticamente cuando se ha cambiado una de las propiedades de un efecto. Sin embargo, las transformaciones se pueden actualizar en cualquiera de los métodos del efecto: como inicializar o los métodos de establecedor de propiedad del efecto.

Por ejemplo, si un efecto contenía un [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) y desea modificar su valor de desplazamiento en respuesta a la propiedad de desplazamiento del efecto que se está cambiando, agregaría el código siguiente en [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a>Crear una transformación personalizada

Para implementar las operaciones de imagen más allá de lo que se proporciona en [Direct2D](./direct2d-portal.md), debe implementar transformaciones personalizadas. Las transformaciones personalizadas pueden cambiar arbitrariamente una imagen de entrada mediante el uso de sombreadores HLSL personalizados.

Las transformaciones implementan una de dos interfaces diferentes en función de los tipos de sombreadores que usan. Las transformaciones que utilizan sombreadores de píxeles o de vértices deben implementar [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), mientras que las transformaciones mediante sombreadores de cálculo deben implementar [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform). Estas interfaces heredan de [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform). Esta sección se centra en la implementación de la funcionalidad que es común a ambos.

La interfaz [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) tiene cuatro métodos para implementar:

### <a name="getinputcount"></a>GetInputCount

Este método devuelve un entero que representa el recuento de entradas de la transformación.


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a>MapInputRectsToOutputRect

[Direct2D](./direct2d-portal.md) llama al método [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) cada vez que se representa la transformación. Direct2D pasa un rectángulo que representa los límites de cada una de las entradas a la transformación. La transformación es responsable de calcular los límites de la imagen de salida. El tamaño de los rectángulos de todos los métodos de esta interfaz ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) se define en píxeles, no en los DIP.

Este método también es responsable de calcular la región de la salida que es opaca en función de la lógica de su sombreador y las regiones opacas de cada entrada. Una región opaca de una imagen se define como donde el canal alfa es ' 1 ' para la totalidad del rectángulo. Si no está claro si la salida de una transformación es opaca, el rectángulo opaco de salida debe establecerse en (0, 0, 0,0) como un valor seguro. [Direct2D](./direct2d-portal.md) usa esta información para realizar optimizaciones de representación con contenido opaco garantizado. Si este valor no es preciso, se puede producir una representación incorrecta.

Puede modificar el comportamiento de representación de la transformación (tal y como se define en las secciones 6 a 8) durante este método. Sin embargo, no puede modificar otras transformaciones en el gráfico de transformación o aquí el diseño del gráfico.


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



Para obtener un ejemplo más complejo, considere cómo se representaría una operación de desenfoque simple:

Si una operación de desenfoque utiliza un radio de 5 píxeles, el tamaño del rectángulo de salida debe expandirse en 5 píxeles, como se muestra a continuación. Al modificar las coordenadas del rectángulo, una transformación debe asegurarse de que su lógica no cause ningún desbordamiento en las coordenadas del rectángulo.


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



Dado que la imagen está borrosa, una región de la imagen que era opaca ahora puede ser parcialmente transparente. Esto se debe a que el área fuera de la imagen tiene como valor predeterminado negro transparente y esta transparencia se combinará en la imagen alrededor de los bordes. La transformación debe reflejar esto en sus cálculos de rectángulo opaco de salida:


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



Estos cálculos se visualizan aquí:

![Ilustración de cálculo de rectángulo.](images/custom-effects2.png)

Para obtener más información sobre este método, consulte la página de referencia de [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .

### <a name="mapoutputrecttoinputrects"></a>MapOutputRectToInputRects

[Direct2D](./direct2d-portal.md) llama al método [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) después de [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). La transformación debe calcular qué parte de la imagen debe leerse para representar correctamente la región de salida solicitada.

Como antes, si un efecto asigna estrictamente los píxeles 1-1, puede pasar el rectángulo de salida a través del rectángulo de entrada:


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



Del mismo modo, si una transformación reduce o expande una imagen (como el ejemplo de desenfoque aquí), los píxeles suelen utilizar píxeles circundantes para calcular su valor. Con un desenfoque, se calcula el promedio de un píxel con sus píxeles circundantes, incluso si están fuera de los límites de la imagen de entrada. Este comportamiento se refleja en el cálculo. Como antes, la transformación comprueba los desbordamientos al expandir las coordenadas de un rectángulo.


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



En esta ilustración se visualiza el cálculo. [Direct2D](./direct2d-portal.md) muestrea automáticamente los píxeles negros transparentes en los que no existe la imagen de entrada, lo que permite mezclar gradualmente el desenfoque con el contenido existente en la pantalla.

![Ilustración de un efecto muestreo de píxeles negros transparentes fuera de un rectángulo.](images/custom-effects3.png)

Si la asignación no es trivial, este método debe establecer el rectángulo de entrada en el área máxima para garantizar resultados correctos. Para ello, establezca los bordes izquierdo y superior en INT \_ min y los bordes inferior y derecho en int \_ máx.

Para obtener más información sobre este método, vea el tema [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .

### <a name="mapinvalidrect"></a>MapInvalidRect

[Direct2D](./direct2d-portal.md) también llama al método [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Sin embargo, a diferencia de los métodos [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) y [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) Direct2D no se garantiza que lo llame en un momento determinado. Este método decide conceptualmente qué parte de la salida de una transformación se debe volver a representar en respuesta a una parte o a todo su cambio de entrada. Hay tres escenarios diferentes para los que se calcula el rectángulo no válido de una transformación.

### <a name="transforms-with-one-to-one-pixel-mapping"></a>Transformaciones con asignación de píxeles de uno a uno

En el caso de las transformaciones que asignan píxeles 1-1, simplemente pase el rectángulo de entrada no válido a través del rectángulo de salida no válido:


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a>Transformaciones con asignación de píxeles de varios a varios

Cuando los píxeles de salida de una transformación dependen de su área circundante, el rectángulo de entrada no válido debe expandirse de forma correspondiente. Esto es para reflejar que los píxeles que rodean el rectángulo de entrada no válido también se verán afectados y dejarán de ser válidos. Por ejemplo, un desenfoque de cinco píxeles usa el siguiente cálculo:


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a>Transformaciones con asignación de píxeles complejos

En el caso de las transformaciones en las que los píxeles de entrada y salida no tienen una asignación simple, todo el resultado se puede marcar como no válido. Por ejemplo, si una transformación simplemente genera el color medio de la entrada, la salida completa de la transformación cambia si se cambia incluso una pequeña parte de la entrada. En este caso, el rectángulo de salida no válido debe establecerse en un rectángulo lógicamente infinito (se muestra a continuación). [Direct2D](./direct2d-portal.md) lo fija automáticamente en los límites de la salida.


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



Para obtener más información sobre este método, vea el tema [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .

Una vez implementados estos métodos, el encabezado de la transformación contendrá lo siguiente:


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a>Agregar un sombreador de píxeles a una transformación personalizada

Una vez creada una transformación, debe proporcionar un sombreador que manipule los píxeles de la imagen. En esta sección se describen los pasos para usar un sombreador de píxeles con una transformación personalizada.

### <a name="implementing-id2d1drawtransform"></a>Implementación de ID2D1DrawTransform

Para usar un sombreador de píxeles, la transformación debe implementar la interfaz [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , que hereda de la interfaz [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) descrita en la sección 5. Esta interfaz contiene un nuevo método para implementar:

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a>SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)

[Direct2D](./direct2d-portal.md) llama al método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) cuando la transformación se agrega por primera vez al gráfico de transformación de un efecto. Este método proporciona un parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) que controla cómo se representa la transformación. Vea el tema **ID2D1DrawInfo** para obtener los métodos disponibles aquí.

Si la transformación decide almacenar este parámetro como una variable de miembro de clase, se puede tener acceso al objeto *drawInfo* y cambiarlo desde otros métodos, como establecedores de propiedad o [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect). En particular, no se puede llamar a desde los métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) o [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) en [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).

### <a name="creating-a-guid-for-the-pixel-shader"></a>Crear un GUID para el sombreador de píxeles

A continuación, la transformación debe definir un GUID único para el propio sombreador de píxeles. Se usa cuando [Direct2D](./direct2d-portal.md) carga el sombreador en la memoria, así como cuando la transformación elige qué sombreador de píxeles se va a usar para la ejecución. Se pueden usar herramientas como guidgen.exe, que se incluye con Visual Studio, para generar un GUID aleatorio.


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a>Cargar el sombreador de píxeles con Direct2D

Un sombreador de píxeles debe cargarse en memoria antes de que lo pueda usar la transformación.

Para cargar el sombreador de píxeles en la memoria, la transformación debe leer el código de byte del sombreador compilado de. Archivo CSO generado por Visual Studio (consulte la documentación de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obtener más detalles) en una matriz de bytes. Esta técnica se muestra en detalle en el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

Una vez que los datos del sombreador se han cargado en una matriz de bytes, llame al método [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) en el objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) del efecto. [Direct2D](./direct2d-portal.md) omite las llamadas a **LoadPixelShader** cuando ya se ha cargado un sombreador con el mismo GUID.

Una vez que se ha cargado un sombreador de píxeles en la memoria, la transformación debe seleccionarlo para su ejecución pasando su GUID al método [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) en el parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) proporcionado durante el método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) . El sombreador de píxeles debe estar ya cargado en la memoria antes de que se seleccione para su ejecución.

### <a name="changing-shader-operation-with-constant-buffers"></a>Cambiar el funcionamiento del sombreador con búferes de constantes

Para cambiar el modo en que se ejecuta un sombreador, una transformación puede pasar un búfer de constantes al sombreador de píxeles. Para ello, una transformación define un struct que contiene las variables deseadas en el encabezado de clase:


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



A continuación, la transformación llama al método [**ID2D1DrawInfo:: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) en el parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) proporcionado en el método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) para pasar este búfer al sombreador.

[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) también debe definir un struct correspondiente que represente el búfer de constantes. Las variables contenidas en el struct del sombreador deben coincidir con las de la estructura de la transformación.


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



Una vez definido el búfer, los valores contenidos en se pueden leer desde cualquier parte del sombreador de píxeles.

### <a name="writing-a-pixel-shader-for-direct2d"></a>Escribir un sombreador de píxeles para Direct2D

Las transformaciones de [Direct2D](./direct2d-portal.md) usan sombreadores creados mediante [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)estándar. Sin embargo, hay algunos conceptos clave para escribir un sombreador de píxeles que se ejecuta desde el contexto de una transformación. Para obtener un ejemplo completo de un sombreador de píxeles totalmente funcional, vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

[Direct2D](./direct2d-portal.md) asigna automáticamente las entradas de una transformación a los objetos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) en HLSL. El primer **Texture2D** se encuentra en el registro T0 y el primer **SamplerState** se encuentra en el registro S0. Cada entrada adicional se encuentra en los siguientes registros correspondientes (T1 y S1, por ejemplo). Los datos de píxeles de una entrada determinada se pueden muestrear llamando a sample en el objeto **Texture2D** y pasando el objeto **SamplerState** correspondiente y las coordenadas textura.

Un sombreador de píxeles personalizado se ejecuta una vez para cada píxel que se representa. Cada vez que se ejecuta el sombreador, [Direct2D](./direct2d-portal.md) proporciona automáticamente tres parámetros que identifican su posición de ejecución actual:

-   Salida de espacio de escena: este parámetro representa la posición de ejecución actual en términos de la superficie de destino general. Se define en píxeles y sus valores Min/Max se corresponden con los límites del rectángulo devuelto por [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).
-   Salida de espacio de recorte: este parámetro lo usa Direct3D y no debe usarse en el sombreador de píxeles de una transformación.
-   Entrada de espacio textura: este parámetro representa la posición de ejecución actual en una textura de entrada determinada. Un sombreador no debe tomar ninguna dependencia sobre cómo se calcula este valor. Solo debe usarlo para muestrear la entrada del sombreador de píxeles, tal como se muestra en el código siguiente:


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a>Agregar un sombreador de vértices a una transformación personalizada

Puede usar sombreadores de vértices para realizar diferentes escenarios de creación de imágenes que los sombreadores de píxeles. En concreto, los sombreadores de vértices pueden realizar efectos de imagen basados en geometría transformando los vértices que componen una imagen. Los sombreadores de vértices se pueden usar de forma independiente o junto con los sombreadores de píxeles especificados por la transformación. Si no se especifica un sombreador de vértices, [Direct2D](./direct2d-portal.md) sustituye en un sombreador de vértices predeterminado para usarlo con el sombreador de píxeles personalizado.

El proceso para agregar un sombreador de vértices a una transformación personalizada es similar al de un sombreador de píxeles: la transformación implementa la interfaz [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , crea un GUID y (opcionalmente) pasa búferes de constantes al sombreador. Sin embargo, hay algunos pasos adicionales clave que son exclusivos de los sombreadores de vértices:

### <a name="creating-a-vertex-buffer"></a>Crear un búfer de vértices

Un sombreador de vértices por definición se ejecuta en los vértices que se le pasan, no en píxeles individuales. Para especificar los vértices para los que se va a ejecutar el sombreador, una transformación crea un búfer de vértice para pasar al sombreador. El diseño de los búferes de vértices está fuera del ámbito de este documento. Vea la [referencia de Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obtener más información o el ejemplo de [SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obtener una implementación de ejemplo.

Después de crear un búfer de vértices en la memoria, la transformación usa el método [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) en el objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) del efecto contenedor para pasar esos datos a la GPU. De nuevo, vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obtener una implementación de ejemplo.

Si no se especifica ningún búfer de vértices mediante la transformación, [Direct2D](./direct2d-portal.md) pasa un búfer de vértices predeterminado que representa la ubicación de la imagen rectangular.

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a>Cambiar SetDrawInfo para que use un sombreador de vértices

Al igual que con los sombreadores de píxeles, la transformación debe cargarse y seleccionar un sombreador de vértices para su ejecución. Para cargar el sombreador de vértices, llama al método [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) en el método [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) recibido en el método Initialize del efecto. Para seleccionar el sombreador de vértices para la ejecución, llama a [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) en el parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) recibido en el método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) de la transformación. Este método acepta un GUID para un sombreador de vértices cargado previamente y, opcionalmente, un búfer de vértice creado previamente para que se ejecute el sombreador.

### <a name="implementing-a-direct2d-vertex-shader"></a>Implementar un sombreador de vértices de Direct2D

Una transformación de dibujo puede contener un sombreador de píxeles y un sombreador de vértices. Si una transformación define un sombreador de píxeles y un sombreador de vértices, la salida del sombreador de vértices se proporciona directamente al sombreador de píxeles: la aplicación puede personalizar la firma devuelta del sombreador de vértices/los parámetros del sombreador de píxeles siempre que sean coherentes.

Por otro lado, si una transformación solo contiene un sombreador de vértices y se basa en el sombreador de píxeles de paso predeterminado de [Direct2D](./direct2d-portal.md), debe devolver la siguiente salida predeterminada:


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



Un sombreador de vértices almacena el resultado de sus transformaciones de vértices en la variable de salida de espacio de la escena del sombreador. Para calcular la salida del espacio de clips y las variables de entrada de espacio textura, [Direct2D](./direct2d-portal.md) proporciona automáticamente matrices de conversión en un búfer de constantes:


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



Se puede encontrar código de sombreador de vértices de ejemplo a continuación que usa las matrices de conversión para calcular el clip correcto y los espacios de textura esperados por [Direct2D](./direct2d-portal.md):


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



El código anterior se puede usar como punto de partida para un sombreador de vértices. Simplemente pasa por la imagen de entrada sin realizar ninguna transformación. De nuevo, vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para una transformación basada en sombreador de vértices totalmente implementada.

Si la transformación no especifica ningún búfer de vértice, [Direct2D](./direct2d-portal.md) sustituye en un búfer de vértices predeterminado que representa la ubicación de la imagen rectangular. Los parámetros para el sombreador de vértices se cambian a los de la salida del sombreador predeterminado:


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



El sombreador de vértices no puede modificar sus parámetros *sceneSpaceOutput* y *clipSpaceOutput* . Debe devolverlos sin cambios. Sin embargo, puede modificar los parámetros *texelSpaceInput* de cada imagen de entrada. Si la transformación también contiene un sombreador de píxeles personalizado, el sombreador de vértices sigue pudiendo pasar parámetros personalizados adicionales directamente al sombreador de píxeles. Además, ya no se proporciona el búfer personalizado de las matrices de conversión *sceneSpace* (b0).

## <a name="adding-a-compute-shader-to-a-custom-transform"></a>Agregar un sombreador de cálculo a una transformación personalizada

Por último, las transformaciones personalizadas pueden emplear sombreadores de cálculo para determinados escenarios de destino. Los sombreadores de cálculo se pueden usar para implementar efectos de imagen complejos que requieren acceso arbitrario a los búferes de imagen de entrada y salida. Por ejemplo, un algoritmo de histograma básico no se puede implementar con un sombreador de píxeles debido a las limitaciones en el acceso a la memoria.

Dado que los sombreadores de cálculo tienen más requisitos de nivel de características de hardware que los sombreadores de píxeles, se deben usar sombreadores de píxeles cuando sea posible para implementar un efecto determinado. En concreto, los sombreadores de cálculo solo se ejecutan en la mayoría de las tarjetas de nivel de DirectX 10 y versiones posteriores. Si una transformación decide usar un sombreador de cálculo, debe comprobar la compatibilidad de hardware adecuada durante la creación de instancias además de implementar la interfaz [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .

### <a name="checking-for-compute-shader-support"></a>Comprobando la compatibilidad del sombreador de cálculo

Si un efecto usa un sombreador de cálculo, debe comprobar la compatibilidad del sombreador de cálculo durante su creación mediante el método [**ID2D1EffectContext:: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) . Si la GPU no admite los sombreadores de cálculo, el efecto debe devolver [**D2DERR \_ insuficientes \_ \_ funcionalidades del dispositivo**](direct2d-error-codes.md).

Hay dos tipos diferentes de sombreadores de cálculo que una transformación puede usar: Shader Model 4 (DirectX 10) y Shader Model 5 (DirectX 11). Hay ciertas limitaciones en los sombreadores modelo 4 de sombreador. Consulte la documentación de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obtener más información. Las transformaciones pueden contener ambos tipos de sombreadores y pueden revertir al modelo de sombreador 4 cuando sea necesario: vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obtener una implementación de este.

### <a name="implement-id2d1computetransform"></a>Implementación de ID2D1ComputeTransform

Esta interfaz contiene dos nuevos métodos que se deben implementar además de los de [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a>SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)

Al igual que con los sombreadores de píxeles y vértices, [Direct2D](./direct2d-portal.md) llama al método [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) cuando la transformación se agrega por primera vez al gráfico de transformación de un efecto. Este método proporciona un parámetro [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) que controla cómo se representa la transformación. Esto incluye elegir el sombreador de cálculo que se va a ejecutar a través del método [**ID2D1ComputeInfo:: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) . Si la transformación decide almacenar este parámetro como una variable de miembro de clase, se puede tener acceso al mismo y cambiarlo desde cualquier método de transformación o efecto con la excepción de los métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) y [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) . Vea el tema **ID2D1ComputeInfo** para ver otros métodos disponibles aquí.

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a>CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)

Mientras que los sombreadores de píxeles se ejecutan por píxel y los sombreadores de vértices se ejecutan por vértices, los sombreadores de cálculo se ejecutan por cada 'threadgroup. Un elemento threadgroup representa un número de subprocesos que se ejecutan simultáneamente en la GPU. El código HLSL del sombreador de cálculo decide cuántos subprocesos se deben ejecutar por elemento threadgroup. El efecto escala el número de threadgroups de forma que el sombreador ejecute el número deseado de veces, en función de la lógica del sombreador.

El método [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) permite a la transformación informar a [Direct2D](./direct2d-portal.md) el número de grupos de subprocesos necesarios, en función del tamaño de la imagen y el conocimiento de la transformación del sombreador.

El número de veces que se ejecuta el sombreador de cálculo es un producto de los recuentos de elemento threadgroup especificados aquí y la anotación ' numthreads ' en el [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)del sombreador de cálculo. Por ejemplo, si la transformación establece las dimensiones elemento threadgroup en (2, 2, 1), el sombreador especifica (3, 3, 1) subprocesos por elemento threadgroup y, a continuación, se ejecutarán 4 threadgroups, cada uno con 9 subprocesos en ellos, para un total de 36 instancias de subproceso.

Un escenario común es procesar un píxel de salida por cada instancia del sombreador de cálculo. Para calcular el número de grupos de subprocesos para este escenario, la transformación divide el ancho y el alto de la imagen por las dimensiones x e y respectivas de la anotación ' numthreads ' en el [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)del sombreador de proceso.

Lo importante es que, si se realiza esta división, el número de grupos de subprocesos solicitados siempre se debe redondear al entero más cercano; de lo contrario, los píxeles de ' resto ' no se ejecutarán en. Si un sombreador (por ejemplo) calcula un solo píxel con cada subproceso, el código del método tendría el siguiente aspecto.


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) usa el siguiente código para especificar el número de subprocesos de cada grupo de subprocesos:


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



Durante la ejecución, el elemento threadgroup actual y el índice del subproceso actual se pasan como parámetros al método de sombreador:


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a>Leer datos de imagen

Los sombreadores de cálculo tienen acceso a la imagen de entrada de la transformación como una sola textura bidimensional:


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



Sin embargo, al igual que los sombreadores de píxeles, no se garantiza que los datos de la imagen empiecen en (0,0) en la textura. En su lugar, [Direct2D](./direct2d-portal.md) proporciona constantes del sistema que permiten a los sombreadores compensar cualquier desplazamiento:


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



Una vez definidos el método auxiliar y el búfer de constantes anteriores, el sombreador puede realizar un muestreo de los datos de imagen mediante lo siguiente:


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a>Escribir datos de imagen

[Direct2D](./direct2d-portal.md) espera que un sombreador defina un búfer de salida para la imagen resultante que se va a colocar. En el modelo de sombreador 4 (DirectX 10), este debe ser un búfer unidimensional debido a las restricciones de características:


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



La textura de salida se indexa primero a fila para permitir que se almacene toda la imagen.


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



Por otro lado, los sombreadores modelo de sombreador 5 (DirectX 11) pueden usar texturas de salida bidimensionales:


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



Con los sombreadores modelo de sombreador 5, [Direct2D](./direct2d-portal.md) proporciona un parámetro ' outputOffset ' adicional en el búfer de constantes. La salida del sombreador debe offsettedse en esta cantidad:


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



A continuación se muestra un sombreador de cálculo del modelo de sombreador de paso 5 completado. En ella, cada uno de los subprocesos del sombreador de cálculo Lee y escribe un solo píxel de la imagen de entrada.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



En el código siguiente se muestra la versión equivalente del modelo de sombreador 4 del sombreador. Observe que el sombreador ahora se representa en un búfer de salida de una sola dimensión.


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 
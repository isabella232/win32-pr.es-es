---
description: Programar DirectX con COM.
title: Programación de DirectX con COM
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 67fc7a35f42439e1a9eeef1b2895d88dc0dbf5d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168013"
---
# <a name="programming-directx-with-com"></a>Programación de DirectX con COM

Microsoft Component Object Model (COM) es un modelo de programación orientado a objetos que usan varias tecnologías, incluida la mayor parte de la superficie de la API de DirectX. Por ese motivo, usted (como desarrollador de DirectX) usa inevitablemente COM al programar DirectX.

> [!NOTE]
> El tema Consume COM components with C++/WinRT (Consumir componentes COM con [C++/WinRT)](/windows/uwp/cpp-and-winrt-apis/consume-com) muestra cómo consumir las API de DirectX (y cualquier API COM, en ese caso) mediante [C++/WinRT.](/windows/uwp/cpp-and-winrt-apis/) Esta es, con diferencia, la tecnología más cómoda y recomendada para usar.

Como alternativa, puede usar COM sin formato y de eso trata este tema. Necesitará un conocimiento básico de los principios y las técnicas de programación implicados en el consumo de API COM. Aunque COM tiene la reputación de ser difícil y complejo, la programación COM requerida por la mayoría de las aplicaciones DirectX es sencilla. En parte, esto se debe a que va a consumir los objetos COM proporcionados por DirectX. No es necesario crear sus propios objetos COM, que normalmente es donde surge la complejidad.

## <a name="com-component-overview"></a>Introducción al componente COM

Un objeto COM es básicamente un componente encapsulado de funcionalidad que las aplicaciones pueden usar para realizar una o varias tareas. Para la implementación, uno o varios componentes COM se empaquetan en un binario denominado servidor COM; con más frecuencia que un archivo DLL.

Un archivo DLL tradicional exporta funciones gratuitas. Un servidor COM puede hacer lo mismo. Pero los componentes COM dentro del servidor COM exponen interfaces COM y métodos de miembro que pertenecen a esas interfaces. La aplicación crea instancias de componentes COM, recupera interfaces de ellos y llama a métodos en esas interfaces para beneficiarse de las características implementadas en los componentes COM.

En la práctica, esto es similar a llamar a métodos en un objeto de C++ normal. Pero hay algunas diferencias.

- Un objeto COM exige una encapsulación más estricta que un objeto de C++. No puede crear simplemente el objeto y, a continuación, llamar a cualquier método público. En su lugar, los métodos públicos de un componente COM se agrupan en una o varias interfaces COM. Para llamar a un método, cree el objeto y recupere del objeto la interfaz que implementa el método . Normalmente, una interfaz implementa un conjunto relacionado de métodos que proporcionan acceso a una característica determinada del objeto. Por ejemplo, la interfaz [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) representa un adaptador de gráficos virtual y contiene métodos que permiten crear recursos, por ejemplo, y muchas otras tareas relacionadas con el adaptador.
- Un objeto COM no se crea de la misma manera que un objeto de C++. Hay varias maneras de crear un objeto COM, pero todas implican técnicas específicas de COM. La API de DirectX incluye una variedad de funciones auxiliares y métodos que simplifican la creación de la mayoría de los objetos COM de DirectX.
- Debe usar técnicas específicas de COM para controlar la duración de un objeto COM.
- No es necesario cargar explícitamente el servidor COM (normalmente un archivo DLL). Tampoco se vincula a una biblioteca estática para usar un componente COM. Cada componente COM tiene un identificador registrado único (un identificador único global, o GUID), que la aplicación usa para identificar el objeto COM. La aplicación identifica el componente y el tiempo de ejecución COM carga automáticamente el archivo DLL de servidor COM correcto.
- COM es una especificación binaria. Se puede escribir en objetos COM y acceder a ellos desde diversos lenguajes. No es necesario saber nada sobre el código fuente del objeto. Por ejemplo, Visual Basic aplicaciones usan rutinariamente objetos COM escritos en C++.

## <a name="component-object-and-interface"></a>Componente, objeto e interfaz

Es importante comprender la distinción entre componentes, objetos e interfaces. En el uso ocasional, es posible que escuche un componente u objeto al que hace referencia el nombre de su interfaz principal. Pero los términos no son intercambiables. Un componente puede implementar cualquier número de interfaces; y un objeto es una instancia de un componente. Por ejemplo, mientras que todos los componentes deben implementar la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), normalmente implementan al menos una interfaz adicional y pueden implementar muchas.

Para usar un método de interfaz determinado, no solo debe crear una instancia de un objeto, sino que también debe obtener la interfaz correcta de él.

Además, más de un componente podría implementar la misma interfaz. Una interfaz es un grupo de métodos que realizan un conjunto de operaciones relacionados lógicamente. La definición de interfaz especifica solo la sintaxis de los métodos y su funcionalidad general. Cualquier componente COM que necesite admitir un conjunto determinado de operaciones puede hacerlo implementando una interfaz adecuada. Algunas interfaces son altamente especializadas y solo se implementan mediante un único componente. otras son útiles en una variedad de circunstancias y se implementan mediante muchos componentes.

Si un componente implementa una interfaz, debe admitir todos los métodos de la definición de interfaz. En otras palabras, debe poder llamar a cualquier método y estar seguro de que existe. Sin embargo, los detalles de cómo se implementa un método determinado pueden variar de un componente a otro. Por ejemplo, los distintos componentes pueden usar algoritmos diferentes para llegar al resultado final. Tampoco hay ninguna garantía de que se admite un método de una manera notrivial. A veces, un componente implementa una interfaz de uso frecuente, pero solo debe admitir un subconjunto de los métodos. Todavía podrá llamar correctamente a los métodos restantes, pero devolverán un [**HRESULT**](#hresult-values) (que es un tipo COM estándar que representa un código de resultado) que contiene el valor **E_NOTIMPL**. Debe consultar su documentación para ver cómo implementa una interfaz cualquier componente determinado.

El estándar COM requiere que una definición de interfaz no debe cambiar una vez publicada. Por ejemplo, el autor no puede agregar un nuevo método a una interfaz existente. En su lugar, el autor debe crear una nueva interfaz. Aunque no hay ninguna restricción sobre los métodos que deben estar en esa interfaz, una práctica común es que la interfaz de próxima generación incluya todos los métodos de la interfaz antigua, además de los métodos nuevos.

No es inusual que una interfaz tenga varias generaciones. Normalmente, todas las generaciones realizan básicamente la misma tarea general, pero son diferentes en detalles específicos. A menudo, un componente COM implementa todas las generaciones actuales y anteriores del linaje de una interfaz determinada. Esto permite que las aplicaciones anteriores sigan usando las interfaces anteriores del objeto, mientras que las aplicaciones más recientes pueden aprovechar las características de las interfaces más recientes. Normalmente, un grupo descendiente de interfaces tiene el mismo nombre, más un entero que indica la generación. Por ejemplo, si la interfaz original se denominase **IMyInterface** (lo que implica la generación 1), las dos generaciones siguientes se llamarían **IMyInterface2** e **IMyInterface3.** En el caso de las interfaces de DirectX, las generaciones sucesivas suelen tener el nombre del número de versión de DirectX.

## <a name="guids"></a>GUID

Los GUID son una parte clave del modelo de programación COM. Como máximo, un GUID es una estructura de 128 bits. Sin embargo, los GUID se crean de tal manera que se garantiza que no hay dos GUID iguales. COM usa los GUID ampliamente para dos propósitos principales.

- Para identificar de forma única un componente COM determinado. Un GUID que se asigna para identificar un componente COM se denomina identificador de clase (CLSID) y se usa un CLSID cuando se desea crear una instancia del componente COM asociado.
- Para identificar de forma única una interfaz COM determinada. Un GUID que se asigna para identificar una interfaz COM se denomina identificador de interfaz (IID) y se usa un IID cuando se solicita una interfaz determinada de una instancia de un componente (un objeto ). El IID de una interfaz será el mismo, independientemente del componente que implemente la interfaz.

Para mayor comodidad, la documentación de DirectX normalmente hace referencia a componentes e interfaces por sus nombres descriptivos (por ejemplo, **ID3D12Device)** en lugar de por sus GUID. En el contexto de la documentación de DirectX, no hay ambigüedad. Técnicamente, es posible que un tercero cree una interfaz con el nombre descriptivo **ID3D12Device** (tendría que tener un IID diferente para ser válido). Sin embargo, en aras de la claridad, no se recomienda.

Por lo tanto, la única manera inequívoca de hacer referencia a un objeto o interfaz determinados es mediante su GUID.

Aunque un GUID es una estructura, un GUID a menudo se expresa en forma de cadena equivalente. El formato general de la forma de cadena de un GUID es de 32 dígitos hexadecimales, con el formato 8-4-4-4-12. Es decir, {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, donde cada x corresponde a un dígito hexadecimal. Por ejemplo, la forma de cadena del IID para la interfaz **ID3D12Device** es {189819F1-1DB6-4B57-BE54-1821339B85F7}.

Dado que el GUID real es un poco complicado de usar y es fácil de escribir mal, normalmente también se proporciona un nombre equivalente. En el código, puede usar este nombre en lugar de la estructura real al llamar a funciones, por ejemplo, cuando se pasa un argumento para el parámetro a `riid` [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice). La convención de nomenclatura habitual es anteponer IID_ o CLSID_ al nombre descriptivo de la interfaz u objeto, respectivamente. Por ejemplo, el nombre del IID de la interfaz **ID3D12Device** es IID_ID3D12Device.

> [!NOTE]
> Las aplicaciones directX deben vincularse ``dxguid.lib`` con y para proporcionar definiciones para los distintos GUID de interfaz ``uuid.lib`` y clase. Visual C++ y otros compiladores admiten la extensión de lenguaje del operador **__uuidof,** pero la vinculación explícita de estilo C con estas bibliotecas de vínculos también es compatible y totalmente portable.

## <a name="hresult-values"></a>Valores HRESULT

La mayoría de los métodos COM devuelven un entero de 32 bits denominado **HRESULT**. Con la mayoría de los métodos, HRESULT es básicamente una estructura que contiene dos elementos principales de información.
- Si el método se ha instalado correctamente o no.
- Información más detallada sobre el resultado de la operación realizada por el método .

Algunos métodos devuelven **un valor HRESULT** del conjunto estándar definido en `Winerror.h` . Sin embargo, un método es libre de devolver un valor **HRESULT** personalizado con información más especializada. Normalmente, estos valores se documentan en la página de referencia del método.

La lista de **valores HRESULT** que se encuentra en la página de referencia de un método suele ser solo un subconjunto de los valores posibles que se pueden devolver. Normalmente, la lista cubre solo los valores específicos del método, así como los valores estándar que tienen algún significado específico del método. Debe suponer que un método puede devolver una variedad de valores **HRESULT** estándar, incluso si no están documentados explícitamente.

Aunque **los valores HRESULT** se usan a menudo para devolver información de error, no debe considerarlos códigos de error. El hecho de que el bit que indica éxito o error se almacena por separado de los bits que contienen la información detallada permite que los valores **HRESULT** tengan cualquier número de códigos correctos y de error. Por convención, los nombres de los códigos de éxito tienen como prefijo S_ y códigos de error por E_. Por ejemplo, los dos códigos más usados son S_OK y E_FAIL, que indican un éxito o un error sencillos, respectivamente.

El hecho de que los métodos COM puedan devolver una variedad de códigos correctos o de error significa que debe tener cuidado al probar el **valor HRESULT.** Por ejemplo, considere un método hipotético con valores devueltos documentados de S_OK si se realiza correctamente y E_FAIL si no es así. Sin embargo, recuerde que el método también puede devolver otros códigos de error o de éxito. El fragmento de código siguiente ilustra el peligro de usar una prueba simple, donde `hr` contiene el **valor HRESULT** devuelto por el método .

```cpp
if (hr == E_FAIL)
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Siempre que, en el caso de error, este método solo devuelva E_FAIL (y no algún otro código de error), esta prueba funciona. Sin embargo, es más realista que se implemente un método determinado para devolver un conjunto de códigos de error específicos, E_NOTIMPL o E_INVALIDARG. Con el código anterior, esos valores se interpretaban incorrectamente como correctos.

Si necesita información detallada sobre el resultado de la llamada al método, debe probar cada valor **HRESULT** pertinente. Sin embargo, es posible que solo le interese si el método se ha hecho correctamente o no. Una manera sólida de probar si un **valor HRESULT** indica que se ha hecho correctamente o no es pasar el valor a una de las siguientes macros, definidas en Winerror.h.

- La `SUCCEEDED` macro devuelve TRUE para un código correcto y FALSE para un código de error.
- La `FAILED` macro devuelve TRUE para un código de error y FALSE para un código correcto.

Por lo tanto, puede corregir el fragmento de código anterior mediante la `FAILED` macro , como se muestra en el código siguiente.

```cpp
if (FAILED(hr))
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Este fragmento de código corregido trata correctamente E_NOTIMPL y E_INVALIDARG errores.

Aunque la mayoría de los métodos COM **devuelven valores HRESULT estructurados,** un número pequeño usa **HRESULT** para devolver un entero simple. Implícitamente, estos métodos siempre son correctos. Si pasa un **valor HRESULT** de este tipo a la macro SUCCEEDED, la macro siempre devuelve TRUE. Un ejemplo de un método comúnmente llamado que no devuelve un **valor HRESULT** es el método **IUnknown::Release,** que devuelve un ULONG. Este método disminuye el recuento de referencias de un objeto en uno y devuelve el recuento de referencias actual. Consulte [Administración de la duración de un](#managing-a-com-objects-lifetime) objeto COM para obtener una explicación del recuento de referencias.

## <a name="the-address-of-a-pointer"></a>Dirección de un puntero

Si ve algunas páginas de referencia de método COM, probablemente se encontrará con algo parecido a lo siguiente.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Aunque un puntero normal es bastante familiar para cualquier desarrollador de C/C++, COM suele usar un nivel adicional de direccionamiento indirecto. Este segundo nivel de direccionamiento indirecto se indica mediante dos asteriscos, , después de la declaración de tipo, y el nombre de la variable normalmente tiene `**` un prefijo de `pp` . Para la función anterior, el parámetro se conoce normalmente `ppDevice` como la dirección de un puntero a un void. En la práctica, en este ejemplo, `ppDevice` es la dirección de un puntero a una interfaz **ID3D12Device.**

A diferencia de un objeto de C++, no se accede directamente a los métodos de un objeto COM. En su lugar, debe obtener un puntero a una interfaz que expone el método . Para invocar el método , se usa básicamente la misma sintaxis que para invocar un puntero a un método de C++. Por ejemplo, para invocar el **método IMyInterface::D oSomething,** usaría la sintaxis siguiente.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

La necesidad de un segundo nivel de direccionamiento indirecto proviene del hecho de que no se crean punteros de interfaz directamente. Debe llamar a uno de los diversos métodos, como el **método D3D12CreateDevice** mostrado anteriormente. Para usar este método para obtener un puntero de interfaz, declare una variable como puntero a la interfaz deseada y, a continuación, pase la dirección de esa variable al método . En otras palabras, se pasa la dirección de un puntero al método . Cuando el método devuelve un resultado, la variable apunta a la interfaz solicitada y puede usar ese puntero para llamar a cualquiera de los métodos de la interfaz.

```cpp
IDXGIAdapter * pIDXGIAdapter = nullptr;
...
ID3D12Device * pD3D12Device = nullptr;
HRESULT hr = ::D3D12CreateDevice(
    pIDXGIAdapter,
    D3D_FEATURE_LEVEL_11_0,
    IID_ID3D12Device,
    &pD3D12Device);
if (FAILED(hr)) return E_FAIL;

// Now use pD3D12Device in the form pD3D12Device->MethodName(...);
```

## <a name="creating-a-com-object"></a>Creación de un objeto COM

Hay varias maneras de crear un objeto COM. Estos son los dos más usados en la programación de DirectX.

- Indirectamente, mediante una llamada a un método o función de DirectX que crea el objeto automáticamente. El método crea el objeto y devuelve una interfaz en el objeto . Cuando se crea un objeto de esta manera, a veces se puede especificar qué interfaz se debe devolver y otras veces la interfaz está implícita. En el ejemplo de código anterior se muestra cómo crear indirectamente un objeto COM de dispositivo Direct3D 12.
- Directamente, pasando el CLSID del objeto a la [**función CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). La función crea una instancia del objeto y devuelve un puntero a una interfaz que especifique.

Una vez, antes de crear objetos COM, debe inicializar COM llamando a la [**función CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Si va a crear objetos indirectamente, el método de creación de objetos controla esta tarea. Sin embargo, si necesita crear un objeto con **CoCreateInstance,** debe llamar explícitamente a **CoInitializeEx.** Cuando haya terminado, COM debe no inicializarse llamando a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Si realiza una llamada a **CoInitializeEx,** debe coincidir con una llamada a **CoUninitialize**. Normalmente, las aplicaciones que necesitan inicializar COM explícitamente lo hacen en su rutina de inicio y desinicializan COM en su rutina de limpieza.

Para crear una nueva instancia de un objeto COM con **CoCreateInstance**, debe tener el CLSID del objeto. Si este CLSID está disponible públicamente, lo encontrará en la documentación de referencia o en el archivo de encabezado adecuado. Si el CLSID no está disponible públicamente, no puede crear el objeto directamente.

La **función CoCreateInstance** tiene cinco parámetros. Para los objetos COM que va a usar con DirectX, normalmente puede establecer los parámetros como se muestra a continuación.

*rclsid* Establezca esta opción en el CLSID del objeto que desea crear.

*pUnkOuter* Establezca en `nullptr` . Este parámetro solo se usa si agrega objetos. Una explicación de la agregación COM está fuera del ámbito de este tema.

*dwClsContext* Establezca en CLSCTX_INPROC_SERVER. Esta configuración indica que el objeto se implementa como un archivo DLL y se ejecuta como parte del proceso de la aplicación.

*riid* Establezca en el IID de la interfaz que le gustaría devolver. La función creará el objeto y devolverá el puntero de interfaz solicitado en el parámetro ppv.

*ppv* Establezca esta propiedad en la dirección de un puntero que se establecerá en la interfaz especificada por `riid` cuando se devuelva la función. Esta variable debe declararse como puntero a la interfaz solicitada y la referencia al puntero de la lista de parámetros debe convertirse como (LPVOID *).

La creación indirecta de un objeto suele ser mucho más sencilla, como vimos en el ejemplo de código anterior. Pasa al método de creación de objetos la dirección de un puntero de interfaz y, a continuación, el método crea el objeto y devuelve un puntero de interfaz. Cuando se crea un objeto indirectamente, incluso si no se puede elegir qué interfaz devuelve el método, a menudo todavía puede especificar una variedad de cosas sobre cómo se debe crear el objeto.

Por ejemplo, puede pasar a **D3D12CreateDevice** un valor que especifique el nivel mínimo de característica D3D que debe admitir el dispositivo devuelto, como se muestra en el ejemplo de código anterior.

## <a name="using-com-interfaces"></a>Uso de interfaces COM

Cuando se crea un objeto COM, el método de creación devuelve un puntero de interfaz. A continuación, puede usar ese puntero para tener acceso a cualquiera de los métodos de la interfaz. La sintaxis es idéntica a la que se usa con un puntero a un método de C++.

## <a name="requesting-additional-interfaces"></a>Solicitar interfaces adicionales

En muchos casos, el puntero de interfaz que recibe del método de creación puede ser el único que necesita. De hecho, es relativamente común que un objeto exporte solo una interfaz que no **sea IUnknown.** Sin embargo, muchos objetos exportan varias interfaces y es posible que necesite punteros a varias de ellas. Si necesita más interfaces que las devueltas por el método de creación, no es necesario crear un nuevo objeto. En su lugar, solicite otro puntero de interfaz mediante el [**método IUnknown::QueryInterface del objeto**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)).

Si crea el objeto con **CoCreateInstance**, puede solicitar un puntero de interfaz **IUnknown** y, a continuación, llamar a **IUnknown::QueryInterface** para solicitar todas las interfaces que necesite. Sin embargo, este enfoque es inconveniente si solo necesita una sola interfaz y no funciona en absoluto si usa un método de creación de objetos que no le permite especificar qué puntero de interfaz se debe devolver. En la práctica, normalmente no es necesario obtener un puntero **IUnknown** explícito, ya que todas las interfaces COM extienden la **interfaz IUnknown.**

Extender una interfaz es conceptualmente similar a heredar de una clase de C++. La interfaz secundaria expone todos los métodos de la interfaz primaria, más uno o varios de los suyos propios. De hecho, a menudo verá que se usa "inherits from" en lugar de "extends". Lo que debe recordar es que la herencia es interna del objeto . La aplicación no puede heredar de ni extender la interfaz de un objeto. Sin embargo, puede usar la interfaz secundaria para llamar a cualquiera de los métodos del elemento secundario o primario.

Dado que todas las interfaces son secundarias de **IUnknown,** puede llamar a **QueryInterface** en cualquiera de los punteros de interfaz que ya tiene para el objeto . Al hacerlo, debe proporcionar el IID de la interfaz que está solicitando y la dirección de un puntero que contendrá el puntero de interfaz cuando el método vuelva.

Por ejemplo, el siguiente fragmento de código llama a **IDXGIFactory2::CreateSwapChainForHwnd** para crear un objeto de cadena de intercambio principal. Este objeto expone varias interfaces. El **método CreateSwapChainForHwnd** devuelve una **interfaz IDXGISwapChain1.** A continuación, el código siguiente usa la interfaz **IDXGISwapChain1** para llamar a **QueryInterface** para solicitar una **interfaz IDXGISwapChain3.**

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;
```

> [!NOTE]
> En C++ puede usar la macro en lugar del IID explícito y ``IID_PPV_ARGS`` el puntero de conversión: ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> A menudo se usa para los métodos de creación, así como **para QueryInterface.** Consulte [combaseapi.h para](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args) obtener más información.

## <a name="managing-a-com-objects-lifetime"></a>Administración de la duración de un objeto COM

Cuando se crea un objeto, el sistema asigna los recursos de memoria necesarios. Cuando ya no se necesita un objeto, se debe destruir. El sistema puede usar esa memoria para otros fines. Con los objetos de C++, puede controlar la duración del objeto directamente con los operadores y en los casos en los que se trabaja en ese nivel, o simplemente mediante la duración de la pila y `new` `delete` el ámbito. COM no permite crear ni destruir objetos directamente. El motivo de este diseño es que más de una parte de la aplicación puede usar el mismo objeto o, en algunos casos, más de una aplicación. Si una de esas referencias destruyese el objeto, las otras referencias no serían válidas. En su lugar, COM usa un sistema de recuento de referencias para controlar la duración de un objeto.

El recuento de referencias de un objeto es el número de veces que se ha solicitado una de sus interfaces. Cada vez que se solicita una interfaz, se incrementa el recuento de referencias. Una aplicación libera una interfaz cuando esa interfaz ya no es necesaria, lo que disminuye el recuento de referencias. Siempre que el recuento de referencias sea mayor que cero, el objeto permanece en memoria. Cuando el recuento de referencias alcanza cero, el objeto se destruye a sí mismo. No es necesario saber nada sobre el recuento de referencias de un objeto. Siempre que obtenga y libere las interfaces de un objeto correctamente, el objeto tendrá la duración adecuada.

Controlar correctamente el recuento de referencias es una parte fundamental de la programación COM. Si no lo hace, puede crear fácilmente una pérdida de memoria o un bloqueo. Uno de los errores más comunes que cometen los programadores COM es no publicar una interfaz. Cuando esto sucede, el recuento de referencias nunca llega a cero y el objeto permanece en memoria indefinidamente.

> [!NOTE]
> Direct3D 10 o posterior ha modificado ligeramente las reglas de duración de los objetos. En concreto, los objetos que se derivan de **ID3DxxDeviceChild** nunca sobreviven a su dispositivo primario (es decir, si el **ID3DxxDevice** propietario alcanza un recuento de referencias 0, todos los objetos secundarios también no son válidos inmediatamente). Además, cuando se usan métodos **Set** para enlazar objetos a la canalización de representación, estas referencias no aumentan el recuento de referencias (es decir, son referencias débiles). En la práctica, esto se controla mejor asegurándose de liberar todos los objetos secundarios del dispositivo por completo antes de liberar el dispositivo.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Incrementar y disminuir el recuento de referencias

Cada vez que se obtiene un nuevo puntero de interfaz, el recuento de referencias se debe incrementar mediante una llamada a [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref). Sin embargo, la aplicación normalmente no necesita llamar a este método. Si obtiene un puntero de interfaz llamando a un método de creación de objetos o llamando a **IUnknown::QueryInterface**, el objeto incrementa automáticamente el recuento de referencias. Sin embargo, si crea un puntero de interfaz de alguna otra manera, como copiar un puntero existente, debe llamar explícitamente a **IUnknown::AddRef**. De lo contrario, al liberar el puntero de interfaz original, el objeto puede destruirse aunque todavía tenga que usar la copia del puntero.

Debe liberar todos los punteros de interfaz, independientemente de si usted o el objeto incrementaron el recuento de referencias. Cuando ya no necesite un puntero de interfaz, llame a [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) para disminuir el recuento de referencias. Una práctica común es inicializar todos los punteros de interfaz en y, a continuación, volver a establecerlos `nullptr` en `nullptr` cuando se liberan. Esa convención permite probar todos los punteros de interfaz en el código de limpieza. Las que no están `nullptr` aún activas y debe liberarlas antes de finalizar la aplicación.

El fragmento de código siguiente amplía el ejemplo mostrado anteriormente para ilustrar cómo controlar el recuento de referencias.

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3Copy = nullptr;

// Make a copy of the IDXGISwapChain3 interface pointer.
// Call AddRef to increment the reference count and to ensure that
// the object is not destroyed prematurely.
pDXGISwapChain3Copy = pDXGISwapChain3;
pDXGISwapChain3Copy->AddRef();
...
// Cleanup code. Check to see whether the pointers are still active.
// If they are, then call Release to release the interface.
if (pDXGISwapChain1 != nullptr)
{
    pDXGISwapChain1->Release();
    pDXGISwapChain1 = nullptr;
}
if (pDXGISwapChain3 != nullptr)
{
    pDXGISwapChain3->Release();
    pDXGISwapChain3 = nullptr;
}
if (pDXGISwapChain3Copy != nullptr)
{
    pDXGISwapChain3Copy->Release();
    pDXGISwapChain3Copy = nullptr;
}
```

## <a name="com-smart-pointers"></a>Punteros inteligentes COM

Hasta ahora, el código ha llamado explícitamente a y para ``Release`` ``AddRef`` mantener los recuentos de referencias mediante **métodos IUnknown.** Este patrón requiere que el programador sea diligente al recordar mantener correctamente el recuento en todas las rutas de código posibles. Esto puede dar lugar a un control de errores complicado y, con el control de excepciones de C++ habilitado, puede ser especialmente difícil de implementar. Una mejor solución con C++ es usar un [puntero inteligente](/cpp/cpp/smart-pointers-modern-cpp).

* **winrt::com_ptr** es un puntero inteligente proporcionado por las proyecciones del lenguaje [C++/WinRT](/uwp/cpp-ref-for-winrt/com-ptr). Este es el puntero inteligente COM recomendado para usar en aplicaciones para UWP. Tenga en cuenta que C++/WinRT requiere C++17.

* **Microsoft::WRL::ComPtr** es un puntero inteligente proporcionado por la biblioteca de plantillas de C++ de [Windows runtime (WRL).](/cpp/cppcx/wrl/comptr-class) Esta biblioteca es C++ "pura", por lo que se puede usar para aplicaciones en tiempo de ejecución de Windows (a través de C++/CX o C++/WinRT), así como aplicaciones de escritorio Win32 clásicas. Este puntero inteligente también funciona en versiones anteriores de Windows que no admiten las API Windows Runtime. En el caso de las aplicaciones de escritorio Win32, puede usar para incluir solo esta clase y, opcionalmente, definir también el ``#include <wrl/client.h>`` símbolo de ``__WRL_CLASSIC_COM_STRICT__`` preprocesador. Para obtener más información, vea [Punteros inteligentes COM revisados.](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited)

* **CComPtr** es un puntero inteligente proporcionado por [el Active Template Library (ATL).](/cpp/atl/reference/ccomptr-class) **Microsoft::WRL::ComPtr** es una versión más reciente de esta implementación que aborda una serie de problemas de uso sutiles, por lo que no se recomienda el uso de este puntero inteligente para nuevos proyectos. Para obtener más información, [vea Creación y uso de CComPtr y CComQIPtr.](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances)


## <a name="using-atl-with-directx-9"></a>Uso de ATL con DirectX 9

Para usar el Active Template Library (ATL) con DirectX 9, debe volver a definir las interfaces para la compatibilidad con ATL. Esto le permite usar correctamente la **clase CComQIPtr** para obtener un puntero a una interfaz.

Sabrá si no vuelve a definir las interfaces para ATL, ya que verá el siguiente mensaje de error.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

En el ejemplo de código siguiente se muestra cómo definir la interfaz IDirectXFileData.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Después de volver a definir la interfaz, debe usar el método **Attach** para adjuntar la interfaz al puntero de interfaz devuelto por **::D irect3DCreate9**. Si no lo hace, la clase de puntero inteligente no liberará correctamente la interfaz **IDirect3D9.**

La **clase CComPtr** llama internamente a **IUnknown::AddRef** en el puntero de interfaz cuando se crea el objeto y cuando se asigna una interfaz a la **clase CComPtr.** Para evitar la pérdida del puntero de interfaz, no llame a **IUnknown::AddRef en la interfaz devuelta desde **::D irect3DCreate9**.

El código siguiente libera correctamente la interfaz sin llamar a **IUnknown::AddRef**.

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Use el código anterior. No use el código siguiente, que llama a **IUnknown::AddRef** seguido de **IUnknown::Release** y no libera la referencia agregada por **::D irect3DCreate9**.

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Tenga en cuenta que este es el único lugar en Direct3D 9 donde tendrá que usar el **método Attach** de esta manera.

Para obtener más información sobre **las clases CComPTR** y **CComQIPtr,** vea sus definiciones en el `Atlbase.h` archivo de encabezado.

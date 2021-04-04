---
title: Solicitar un objeto para una interfaz
description: Solicitar un objeto para una interfaz
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077761"
---
# <a name="asking-an-object-for-an-interface"></a>Solicitar un objeto para una interfaz

Vimos anteriormente que un objeto puede implementar más de una interfaz. El objeto de cuadro de diálogo de elementos comunes es un ejemplo del mundo real. Para admitir los usos más habituales, el objeto implementa la interfaz [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Esta interfaz define métodos básicos para mostrar el cuadro de diálogo y obtener información sobre el archivo seleccionado. Sin embargo, para un uso más avanzado, el objeto también implementa una interfaz denominada [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Un programa puede utilizar esta interfaz para personalizar la apariencia y el comportamiento del cuadro de diálogo, agregando nuevos controles de IU.

Recuerde que todas las interfaces COM deben heredar directa o indirectamente de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . En el diagrama siguiente se muestra la herencia del objeto de cuadro de diálogo de elementos comunes.

![diagrama que muestra las interfaces expuestas por el objeto de cuadro de diálogo de elementos comunes](images/com06.png)

Como puede ver en el diagrama, el antecesor directo de [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) es la interfaz [**IFileDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , que a su vez hereda [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). Al subir la cadena de herencia de **IFileOpenDialog** a **IModalWindow**, las interfaces definen la funcionalidad de ventana generalizada cada vez más. Por último, la interfaz **IModalWindow** hereda [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). El objeto de cuadro de diálogo Common Item también implementa [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), que existe en una cadena de herencia independiente.

Ahora Supongamos que tiene un puntero a la interfaz [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . ¿Cómo obtendría un puntero a la interfaz [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?

![diagrama que muestra dos punteros de interfaz a interfaces en el mismo objeto](images/com07.png)

Simplemente no funcionará la conversión del puntero [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) a un puntero [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) . No hay ninguna manera confiable de "conversión cruzada" a través de una jerarquía de herencia, sin alguna forma de información de tipo en tiempo de ejecución (RTTI), que es una característica que depende de gran parte del lenguaje.

El enfoque de COM consiste en *pedir* al objeto que le proporcione un puntero [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , usando la primera interfaz como conducto en el objeto. Esto se hace llamando al método [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) desde el primer puntero de interfaz. Puede pensar en **QueryInterface** como una versión independiente del lenguaje de la palabra clave de **\_ conversión dinámica** en C++.

El método [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) tiene la firma siguiente:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

En función de lo que ya conoce en [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), es posible que pueda adivinar cómo funciona [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

-   El parámetro *riid* es el GUID que identifica la interfaz que se solicita. El tipo de datos **REFIID** es un **typedef** para `const GUID&` . Observe que el identificador de clase (CLSID) no es necesario, porque el objeto ya se ha creado. Solo es necesario el identificador de interfaz.
-   El parámetro *ppvObject* recibe un puntero a la interfaz. El tipo de datos de este parámetro **es \* \* void**, por la misma razón que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa este tipo de datos: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) se puede usar para consultar cualquier interfaz com, por lo que el parámetro no puede tener un tipo seguro.

Aquí se muestra cómo llamaría a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



Como siempre, compruebe el valor devuelto **HRESULT** en caso de que se produzca un error en el método. Si el método se ejecuta correctamente, debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando haya terminado de usar el puntero, tal como se describe en [Administración de la duración de un objeto](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Siguientes

[Asignación de memoria en COM](memory-allocation-in-com.md)

 

 
---
title: Pedir un objeto para una interfaz
description: Pedir un objeto para una interfaz
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fa740f0ef770e069ee03b644bbfcb9b2c5e0eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160007"
---
# <a name="asking-an-object-for-an-interface"></a>Pedir un objeto para una interfaz

Anteriormente vimos que un objeto puede implementar más de una interfaz. El objeto Common Item Dialog es un ejemplo real de esto. Para admitir los usos más típicos, el objeto implementa la [**interfaz IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) Esta interfaz define métodos básicos para mostrar el cuadro de diálogo y obtener información sobre el archivo seleccionado. Sin embargo, para un uso más avanzado, el objeto también implementa una interfaz denominada [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Un programa puede usar esta interfaz para personalizar la apariencia y el comportamiento del cuadro de diálogo mediante la adición de nuevos controles de interfaz de usuario.

Recuerde que todas las interfaces COM deben heredar, directa o indirectamente, de [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) En el diagrama siguiente se muestra la herencia del objeto Cuadro de diálogo de elemento común.

![diagrama que muestra las interfaces expuestas por el objeto de diálogo de elemento común](images/com06.png)

Como puede ver en el diagrama, el antecesor directo de [**IFileOpenDialog**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) es la [**interfaz IFileDialog,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) que a su vez hereda [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). A medida que suba la cadena de herencia de **IFileOpenDialog** a **IModalWindow,** las interfaces definen una funcionalidad de ventana cada vez más generalizada. Por último, **la interfaz IModalWindow** hereda [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). El objeto Cuadro de diálogo de elemento común también [**implementa IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), que existe en una cadena de herencia independiente.

Ahora supongamos que tiene un puntero a la [**interfaz IFileOpenDialog.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) ¿Cómo se obtiene un puntero a la [**interfaz IFileDialogCustomize?**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)

![diagrama que muestra dos punteros de interfaz a interfaces en el mismo objeto](images/com07.png)

Convertir el puntero [**IFileOpenDialog en**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) un [**puntero IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) no funcionará. No hay ninguna manera confiable de "conversión cruzada" en una jerarquía de herencia, sin algún tipo de información de tipo en tiempo de ejecución (RTTI), que es una característica altamente dependiente del lenguaje.

El enfoque COM es *pedir* al objeto que le dé un puntero [**IFileDialogCustomize,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) usando la primera interfaz como un conduit en el objeto . Para ello, llame al [**método IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) desde el primer puntero de interfaz. Puede pensar en **QueryInterface como** una versión independiente del lenguaje de la palabra clave **de \_ conversión** dinámica en C++.

El [**método QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) tiene la firma siguiente:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

En función de lo que ya sabe sobre [**CoCreateInstance,**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)es posible que pueda adivinar cómo [**funciona QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))

-   El *parámetro riid* es el GUID que identifica la interfaz que está solicitando. El tipo de **datos REFIID** es una **definición de tipo** para `const GUID&` . Observe que el identificador de clase (CLSID) no es necesario, porque el objeto ya se ha creado. Solo es necesario el identificador de interfaz.
-   El *parámetro ppvObject* recibe un puntero a la interfaz . El tipo de datos de este parámetro es **\* \* void,** por la misma razón por la que [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa este tipo de datos: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) se puede usar para consultar cualquier interfaz COM, por lo que el parámetro no se puede escribir fuertemente.

Aquí se muestra cómo llamaría [**a QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un [**puntero IFileDialogCustomize:**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize)


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



Como siempre, compruebe el valor **devuelto HRESULT,** en caso de que se produce un error en el método. Si el método se realiza correctamente, debe llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cuando haya terminado de usar el puntero , como se describe en Administración de la duración [de un objeto](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Siguientes

[Asignación de memoria en COM](memory-allocation-in-com.md)

 

 
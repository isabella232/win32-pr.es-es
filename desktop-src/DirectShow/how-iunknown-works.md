---
description: Cómo funciona IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Cómo funciona IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7549ce892e9c0dd3c82f1229a2440f1b930190
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151981"
---
# <a name="how-iunknown-works"></a>Cómo funciona IUnknown

Los métodos de **IUnknown** permiten que una aplicación consulte las interfaces del componente y administre el recuento de referencias del componente.

**Recuento de referencias**

El recuento de referencias es una variable interna, incrementada en el método **AddRef** y disminuida en el método **Release** . Las clases base administran el recuento de referencias y sincronizan el acceso al recuento de referencias entre varios subprocesos.

**Consultas de interfaz**

La consulta de una interfaz también es sencilla. El autor de la llamada pasa dos parámetros: un identificador de interfaz (IID) y la dirección de un puntero. Si el componente admite la interfaz solicitada, establece el puntero en la interfaz, incrementa su propio recuento de referencias y devuelve S \_ OK. De lo contrario, establece el puntero en **null** y devuelve e \_ nointerface. En el siguiente pseudocódigo se muestra el esquema general del método **QueryInterface** . La agregación de componentes, que se describe en la sección siguiente, presenta cierta complejidad adicional.


```C++
if (IID == IID_IUnknown)
    set pointer to (IUnknown *)this
    AddRef
    return S_OK

else if (IID == IID_ISomeInterface)
    set pointer to (ISomeInterface *)this
    AddRef
    return S_OK

else if ... 

else
    set pointer to NULL
    return E_NOINTERFACE
```



La única diferencia entre el método **QueryInterface** de un componente y el método **QueryInterface** de otro es la lista de IID que prueba cada componente. Para cada interfaz que admite el componente, el componente debe probar el IID de esa interfaz.

**Agregación y delegación**

La agregación de componentes debe ser transparente para el autor de la llamada. Por lo tanto, el agregado debe exponer una única interfaz **IUnknown** , con el componente agregado que aplaza la implementación del componente externo. De lo contrario, el autor de la llamada verá dos interfaces **IUnknown** diferentes en el mismo agregado. Si no se agrega el componente, utiliza su propia implementación.

Para admitir este comportamiento, el componente debe agregar un nivel de direccionamiento indirecto. La *delegación de IUnknown* delega el trabajo en el lugar adecuado: para el componente externo, si hay alguno, o para la versión interna del componente. Un *IUnknown sin delegación* realiza el trabajo, tal como se describe en la sección anterior.

La versión de delegación es pública y mantiene el nombre **IUnknown**. Se cambia el nombre de la versión no delegada [**INonDelegatingUnknown**](inondelegatingunknown.md). Este nombre no forma parte de la especificación COM, porque no es una interfaz pública.

Cuando el cliente crea una instancia del componente, llama al método **IClassFactory:: CreateInstance** . Un parámetro es un puntero a la interfaz **IUnknown** del componente de agregado, o **null** si no se agrega la nueva instancia. El componente utiliza este parámetro para almacenar una variable miembro que indica qué interfaz **IUnknown** se va a usar, como se muestra en el ejemplo siguiente:


```C++
CMyComponent::CMyComponent(IUnknown *pOuterUnkown)
{
    if (pOuterUnknown == NULL)
        m_pUnknown = (IUnknown *)(INonDelegatingUnknown *)this;
    else
        m_pUnknown = pOuterUnknown;

    [ ... more constructor code ... ]
}
```



Cada método en el **IUnknown** de delegación llama a su homólogo no delegado, como se muestra en el ejemplo siguiente:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Según la naturaleza de la delegación, los métodos de delegación son idénticos en todos los componentes. Solo cambian las versiones sin delegación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




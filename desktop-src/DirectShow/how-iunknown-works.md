---
description: Funcionamiento de IUnknown
ms.assetid: 926778a5-e941-4424-8bc0-b50c925fd08b
title: Funcionamiento de IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1523a8de5d9b99df60ebaff540d4bf9468799e3be1361a4be111f15a142bbea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015593"
---
# <a name="how-iunknown-works"></a>Funcionamiento de IUnknown

Los métodos **de IUnknown permiten** a una aplicación consultar interfaces en el componente y administrar el recuento de referencias del componente.

**Recuento de referencias**

El recuento de referencias es una variable interna, incrementada en el **método AddRef** y disminuyeda en el **método Release.** Las clases base administran el recuento de referencias y sincronizan el acceso al recuento de referencias entre varios subprocesos.

**Consultas de interfaz**

La consulta de una interfaz también es sencilla. El autor de la llamada pasa dos parámetros: un identificador de interfaz (IID) y la dirección de un puntero. Si el componente admite la interfaz solicitada, establece el puntero a la interfaz, incrementa su propio recuento de referencias y devuelve S \_ OK. De lo contrario, establece el puntero en **NULL** y devuelve E \_ NOINTERFACE. El pseudocódigo siguiente muestra el esquema general del **método QueryInterface.** La agregación de componentes, que se describe en la sección siguiente, presenta cierta complejidad adicional.


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



La única diferencia entre el **método QueryInterface** de un componente y el método **QueryInterface** de otro es la lista de IID que prueba cada componente. Para cada interfaz que admita el componente, el componente debe probar el IID de esa interfaz.

**Agregación y delegación**

La agregación de componentes debe ser transparente para el autor de la llamada. Por lo tanto, el agregado debe exponer una única interfaz **IUnknown,** con el componente agregado aplazando a la implementación del componente externo. De lo contrario, el autor de la llamada vería dos **interfaces IUnknown** diferentes en el mismo agregado. Si el componente no se agrega, usa su propia implementación.

Para admitir este comportamiento, el componente debe agregar un nivel de direccionamiento indirecto. Un *IUnknown* delegado delega el trabajo en el lugar adecuado: en el componente externo, si hay uno, o en la versión interna del componente. Un *IUnknown* no delegado realiza el trabajo, como se describe en la sección anterior.

La versión de delegación es pública y mantiene el nombre **IUnknown.** El nombre de la versión no delegating se denomina [**INonDelegatingUnknown.**](inondelegatingunknown.md) Este nombre no forma parte de la especificación COM, porque no es una interfaz pública.

Cuando el cliente crea una instancia del componente, llama al **método IClassFactory::CreateInstance.** Un parámetro es un puntero a la interfaz **IUnknown** del componente de agregación o **NULL** si no se agrega la nueva instancia. El componente usa este parámetro para almacenar una variable miembro que indica qué **interfaz IUnknown** se va a usar, como se muestra en el ejemplo siguiente:


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



Cada método del **IUnknown** delegado llama a su homólogo no delegado, como se muestra en el ejemplo siguiente:


```C++
HRESULT QueryInterface(REFIID iid, void **ppv) 
{
    return m_pUnknown->QueryInterface(iid, ppv);
}
```



Por la naturaleza de la delegación, los métodos de delegación parecen idénticos en cada componente. Solo cambian las versiones no delegadas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




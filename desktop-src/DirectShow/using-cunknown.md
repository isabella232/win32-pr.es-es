---
description: DirectShow implementa IUnknown en una clase base denominada CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Usar CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667859"
---
# <a name="using-cunknown"></a>Usar CUnknown

DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) en una clase base denominada [**CUnknown**](cunknown.md). Puede usar **CUnknown** para derivar otras clases, invalidando solo los métodos que cambian en los componentes. La mayoría de las otras clases base de DirectShow se derivan de **CUnknown**, por lo que el componente puede heredar directamente de **CUnknown** o de otra clase base.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md). Administra los recuentos de referencias internamente y, en la mayoría de los casos, la clase derivada puede heredar los dos métodos de recuento de referencias sin ningún cambio. Tenga en cuenta que **CUnknown** se elimina a sí mismo cuando el recuento de referencias desciende a cero. Por otro lado, debe invalidar [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), porque el método de la clase base devuelve E \_ nointerface si recibe un IID distinto de IID \_ IUnknown. En la clase derivada, compruebe los IID de las interfaces que admite, tal como se muestra en el ejemplo siguiente:


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



La función de utilidad [**GetInterface**](getinterface.md) (vea [**funciones auxiliares de com**](com-helper-functions.md)) establece el puntero, incrementa el recuento de referencias de una manera segura para subprocesos y devuelve S \_ correctos. En el caso predeterminado, llame al método de la clase base y devuelva el resultado. Si deriva de otra clase base, llame a su método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) en su lugar. Esto le permite admitir todas las interfaces que admite la clase primaria.

## <a name="iunknown"></a>IUnknown

Como se mencionó anteriormente, la versión de delegación de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es la misma para todos los componentes, ya que no hace nada más que invocar la instancia correcta de la versión sin delegación. Para mayor comodidad, el archivo de encabezado ComBase. h contiene una macro, [**declare \_ IUNKNOWN**](declare-iunknown.md), que declara los tres métodos de delegación como métodos insertados. Se expande al siguiente código:


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



La función de utilidad [**CUnknown:: GetOwner**](cunknown-getowner.md) recupera un puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del componente que posee este componente. Para un componente agregado, el propietario es el componente externo. De lo contrario, el componente es el propietario. Incluya la macro declare \_ IUNKNOWN en la sección Public de la definición de clase.

## <a name="class-constructor"></a>Constructor de clase

El constructor de clase debe invocar el método de constructor de la clase primaria, además de cualquier cosa que sea específica de la clase. El ejemplo siguiente es un método de constructor típico:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



El método toma los parámetros siguientes, que pasa directamente al método de constructor [**CUnknown**](cunknown.md) .

-   *tszName* especifica un nombre para el componente.
-   *pUnk* es un puntero a la [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)de agregación.
-   *pHr* es un puntero a un valor HRESULT que indica si el método se ha ejecutado correctamente o no.

## <a name="summary"></a>Resumen

En el ejemplo siguiente se muestra una clase derivada que admite [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y una interfaz hipotética denominada ISomeInterface:


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



En este ejemplo se muestran los puntos siguientes:

-   La clase [**CUnknown**](cunknown.md) implementa la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . El nuevo componente hereda de **CUnknown** y de cualquier interfaz que el componente admita. El componente podría derivar en su lugar de otra clase base que hereda de **CUnknown**.
-   La macro [**declare \_ IUnknown**](declare-iunknown.md) declara los métodos de delegación de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) como métodos insertados.
-   La clase [**CUnknown**](cunknown.md) proporciona la implementación de [**INonDelegatingUnknown**](inondelegatingunknown.md).
-   Para admitir una interfaz que no sea [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la clase derivada debe reemplazar el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) y probar el IID de la nueva interfaz.
-   El constructor de clase invoca el método de constructor para [**CUnknown**](cunknown.md).

El paso siguiente para escribir un filtro consiste en permitir que una aplicación cree nuevas instancias del componente. Esto requiere un conocimiento de los archivos dll y su relación con los generadores de clases y los métodos de constructor de clase. Para obtener más información, vea [Cómo crear un archivo dll de filtro de DirectShow](how-to-create-a-dll.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 

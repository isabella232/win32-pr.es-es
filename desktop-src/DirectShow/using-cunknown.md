---
description: DirectShow implementa IUnknown en una clase base denominada CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Uso de CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211ebf8c581502665c5f07b3720759efc7afab75a05a49a68f9945029dd6cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051385"
---
# <a name="using-cunknown"></a>Uso de CUnknown

DirectShow implementa [**IUnknown en**](/windows/win32/api/unknwn/nn-unknwn-iunknown) una clase base denominada [**CUnknown**](cunknown.md). Puede usar **CUnknown para** derivar otras clases, reemplazando solo los métodos que cambian entre componentes. La mayoría de las demás clases base de DirectShow derivan de **CUnknown,** por lo que el componente puede heredar directamente de **CUnknown** o de otra clase base.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md). Administra los recuentos de referencias internamente y, en la mayoría de los casos, la clase derivada puede heredar los dos métodos de recuento de referencias sin cambios. Tenga en cuenta **que CUnknown** se elimina cuando el recuento de referencias cae a cero. Por otro lado, debe invalidar [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), porque el método de la clase base devuelve E NOINTERFACE si recibe un IID que no sea \_ \_ IUnknown de IID. En la clase derivada, pruebe los IID de las interfaces que admite, como se muestra en el ejemplo siguiente:


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



La función de utilidad [**GetInterface**](getinterface.md) (vea Funciones auxiliares [**COM)**](com-helper-functions.md)establece el puntero, incrementa el recuento de referencias de una manera segura para subprocesos y devuelve S \_ OK. En el caso predeterminado, llame al método de clase base y devuelva el resultado. Si deriva de otra clase base, llame a su [**método NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) en su lugar. Esto le permite admitir todas las interfaces que admite la clase primaria.

## <a name="iunknown"></a>IUnknown

Como se mencionó anteriormente, la versión de delegación de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) es la misma para cada componente, ya que no hace nada más que invocar la instancia correcta de la versión no delegada. Para mayor comodidad, el archivo de encabezado Combase.h contiene una macro, [**DECLARE \_ IUNKNOWN**](declare-iunknown.md), que declara los tres métodos de delegación como métodos en línea. Se expande al código siguiente:


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



La función de [**utilidad CUnknown::GetOwner**](cunknown-getowner.md) recupera un puntero a la [**interfaz IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del componente que posee este componente. Para un componente agregado, el propietario es el componente externo. De lo contrario, el componente se posee a sí mismo. Incluya la macro DECLARE \_ IUNKNOWN en la sección pública de la definición de clase.

## <a name="class-constructor"></a>Constructor de clase

El constructor de clase debe invocar el método de constructor para la clase primaria, además de todo lo que haga que sea específico de la clase. El ejemplo siguiente es un método de constructor típico:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



El método toma los parámetros siguientes, que pasa directamente al método de constructor [**CUnknown.**](cunknown.md)

-   *tszName especifica* un nombre para el componente.
-   *pUnk* es un puntero al [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)que agrega .
-   *pHr* es un puntero a un valor HRESULT, que indica el éxito o el error del método.

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

-   La [**clase CUnknown**](cunknown.md) implementa la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) El nuevo componente hereda de **CUnknown y** de cualquier interfaz que admita el componente. El componente podría derivarse en su lugar de otra clase base que herede de **CUnknown**.
-   La [**macro DECLARE \_ IUNKNOWN**](declare-iunknown.md) declara los métodos [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) delegados como métodos en línea.
-   La [**clase CUnknown**](cunknown.md) proporciona la implementación de [**INonDelegatingUnknown.**](inondelegatingunknown.md)
-   Para admitir una interfaz que no sea [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown)la clase derivada debe invalidar el método [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) y probar el IID de la nueva interfaz.
-   El constructor de clase invoca el método de constructor para [**CUnknown**](cunknown.md).

El siguiente paso para escribir un filtro es permitir que una aplicación cree nuevas instancias del componente. Esto requiere una comprensión de los archivos DLL y su relación con los generadores de clases y los métodos de constructor de clases. Para obtener más información, [vea How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo implementar IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 

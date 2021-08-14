---
title: Ejemplo para resolver conflictos de nombre de función
description: En este tema se describe cómo resolver conflictos de nombres de función al crear una extensión para ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, código de ejemplo Visual Basic , resolver conflictos de nombres de función
- resolver conflictos de nombres de función ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6ce09251ba61b31768d973e258c568694067aff0420f0512a13913bb6fce90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179985"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Ejemplo para resolver conflictos de nombre de función

Tenga en cuenta lo siguiente.

-   IADs0 no admite Func0.
-   IADs1 admite Func1 y Func0.
-   IADs2 admite Func2 y Func0.

Las tres interfaces son interfaces duales.


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



Tenga en cuenta que, aunque IADs1 no admite Func2, un cliente ADSI reconoce un [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que admite todas las interfaces duales y de distribución del modelo. Por lo tanto, el cliente ADSI puede llamar directamente a Func2 mediante myInf1.Func2 sin resolver qué interfaz admite Func2.


```VB
myInf1.Func2
```



Tanto IADs1 como IADs2 tienen una función denominada Func0, pero los IADs1::Func0 se invocan directamente mediante el acceso vtable, ya que los dos elementos siguientes se aplican al cliente:

-   El cliente tiene un puntero al objeto IADs1 de interfaz dual, que tiene una función denominada Func0.
-   Visual Basic admite el acceso directo a vtable, suponiendo que ese tipo de datos esté disponible a través de la biblioteca de tipos.

En el ejemplo de código siguiente, el cliente tiene un puntero de interfaz dual a IADs2 en lugar de a IADs1. Por lo tanto, se invoca IADs2::Func0 mediante el acceso directo a vtable.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



De nuevo, en el ejemplo de código siguiente, tanto IADs1 como IADs2 tienen una función denominada Func0, pero, aquí, el cliente tiene un puntero a una interfaz dual, IADs0, que no tiene una función denominada Func0. Por lo tanto, no se puede realizar ningún acceso directo a vtable. En su [**lugar, se llama a IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) para invocar Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Tenga en cuenta estos dos casos:

-   Los IADs1 e IAD2 se implementan mediante dos componentes COM, Ext1 y Ext2, respectivamente. Si Ext1 va antes que Ext2 en el Registro, se invoca IADs1::Func0. Sin embargo, si Ext2 aparece primero en el Registro, se invoca IADs2::Func0.
-   Si IADs1 y ADs2 se implementan mediante el mismo objeto de extensión, los [**métodos IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) siempre invocan Func0.

El desarrollador de extensiones debe determinar cómo resolver conflictos de funciones o propiedades de diferentes interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales que tienen el mismo nombre en una extensión. La implementación de [**los métodos IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) debe resolver este conflicto. Por ejemplo, si usa IMyInterface1::Func1 e IMyInterface2::Func1, donde IMyInterface1 e IMyInterface2 son interfaces **IDispatch** duales compatibles con el mismo objeto de extensión. Los **métodos PrivateGetIDsOfNames** y **PrivateInvoke** deben determinar a qué Func1 siempre se debe llamar.

Lo mismo se aplica a los DISPID en conflicto en diferentes interfaces duales [**o IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

Por ejemplo, dispid de IMyInterface1::Y es 2 en el archivo imyinterface1.odl o imyinterface1.idl. El DISPID de IMyInterface2::X también es 2 en iMyInterface2.odl. [**IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) debe devolver un DISPID único, dentro de la propia extensión, para cada uno, en lugar de devolver el mismo DISPID para ambos.

ADSI resuelve el primer problema al no admitir varias interfaces con nombres de función o propiedad en conflicto. Resuelve el segundo problema agregando un único, que se encuentra dentro del mismo objeto de extensión, número de interfaz a los bits no usados de DISPID.

 

 
---
title: Ejemplo para resolver conflictos de nombres de función
description: En este tema se describe cómo resolver conflictos de nombres de función al crear una extensión para ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Visual Basic de código de ejemplo, resolver conflictos de nombres de función
- resolver conflictos de nombre de función ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359417"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Ejemplo para resolver conflictos de nombres de función

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



Tenga en cuenta que, a pesar de que IADs1 no admite Func2, un cliente ADSI reconoce una [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que admite todas las interfaces dual y de distribución del modelo. Por lo tanto, el cliente ADSI puede llamar directamente a Func2 mediante myInf1. Func2 sin resolver qué interfaz es compatible con Func2.


```VB
myInf1.Func2
```



Tanto IADs1 como IADs2 tienen una función llamada Func0, pero IADs1:: Func0 se invoca directamente mediante el acceso vtable, porque las dos siguientes se aplican al cliente:

-   El cliente tiene un puntero a un objeto IADs1 de interfaz dual, que tiene una función denominada Func0.
-   Visual Basic admite el acceso de vtable directo, suponiendo que ese tipo de datos esté disponible a través de la biblioteca de tipos.

En el ejemplo de código siguiente, el cliente tiene un puntero de interfaz dual a IADs2 en lugar de IADs1. Por lo tanto, IADs2:: Func0 se invoca mediante el acceso de vtable directo.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



De nuevo, en el ejemplo de código siguiente, IADs1 y IADs2 tienen una función llamada Func0, pero, aquí, el cliente tiene un puntero a una interfaz dual, IADs0, que no tiene una función llamada Func0. Por lo tanto, no se puede realizar ningún acceso de vtable directo. En su lugar, se llama a [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) para invocar Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Tenga en cuenta estos dos casos:

-   IADs1 y IADs2 se implementan mediante dos componentes COM, EXT1 y ext2, respectivamente. Si EXT1 va antes de ext2 en el registro, se invoca IADs1:: Func0. Sin embargo, si ext2 aparece primero en el registro, se invoca IADs2:: Func0.
-   Si IADs1 y ADs2 se implementan mediante el mismo objeto de extensión, los métodos [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) de la extensión siempre invocan a Func0.

El desarrollador de la extensión debe determinar cómo resolver conflictos de funciones, o propiedades, de diferentes interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duales que tienen el mismo nombre en una extensión. La implementación de [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) y los métodos [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deben resolver este conflicto. Por ejemplo, si usa IMyInterface1:: Func1 y IMyInterface2:: Func1, donde IMyInterface1 y IMyInterface2 son interfaces **IDispatch** duales admitidas por el mismo objeto de extensión. Los métodos **PrivateGetIDsOfNames** y **PrivateInvoke** deben determinar a qué Func1 se debe llamar siempre.

Lo mismo se aplica a los DISPID conflictivos en diferentes interfaces dobles o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

Por ejemplo, el DISPID de IMyInterface1:: Y es 2 en el archivo IMyInterface1. ODL o IMyInterface1. idl. El DISPID de IMyInterface2:: X también es 2 en iMyInterface2. ODL. [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) debe devolver un DISPID único, dentro de la propia extensión, para cada, en lugar de devolver el mismo DISPID para ambos.

ADSI resuelve el primer problema al no admitir varias interfaces con nombres de función o propiedad en conflicto. Resuelve el segundo problema agregando un único, que está en el mismo objeto de extensión, el número de la interfaz a los bits sin usar del DispId.

 

 
---
title: Interfaces duales IAccessible e IDispatch
description: Los desarrolladores de servidores deben proporcionar la interfaz IDispatch del Modelo de objetos componentes (COM) estándar para sus objetos accesibles.
ms.assetid: 043d6777-6f9a-4e93-aadc-9cbe9a9119c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bbe19e35a04414253dc8f22c4edbc19a041b27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359116"
---
# <a name="dual-interfaces-iaccessible-and-idispatch"></a>Interfaces duales: IAccessible e IDispatch

Los desarrolladores de servidores deben proporcionar la interfaz [**IDispatch**](idispatch-interface.md) del Modelo de objetos componentes (COM) estándar para sus objetos accesibles. La interfaz IDispatch permite que las aplicaciones cliente escritas en Microsoft Visual Basic y varios lenguajes de scripting usen los métodos y propiedades expuestos por [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Dado que un objeto accesible proporciona acceso a un objeto indirectamente a través de [IDispatch::Invoke]( /windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) o directamente con **IAccessible,** se dice que tiene una interfaz dual.

Cuando los clientes de C/C++ obtienen un puntero de interfaz IDispatch, los clientes pueden llamar a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para intentar convertir el puntero de interfaz IDispatch en un puntero de interfaz [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Para llamar indirectamente a **los métodos IAccessible,** los clientes de C/C++ llaman a IDispatch::Invoke. Para mejorar el rendimiento, llame a los **métodos IAccessible** para usar el objeto directamente.

Para obtener una lista de los id. de envío (DISPID) que **IDispatch** usa para identificar los métodos y propiedades [**de IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vea apéndice [C: IAccessible DISPIDs (Apéndice C: IAccessible DISPIDs](appendix-c--iaccessible-dispids.md)).

> [!Note]  
> En la versión 2.0 y posteriores de Microsoft Active Accessibility, los servidores no tienen que implementar completamente los métodos de [**IDispatch,**](idispatch-interface.md) sino que simplemente pueden devolver E NOTIMPL después de inicializar los parámetros out, como se muestra en el \_ ejemplo siguiente.

 


```C++
HRESULT STDMETHODCALLTYPE AccServer::GetTypeInfoCount(UINT* pctinfo)
{
    *pctinfo = 0;
    return E_NOTIMPL;
};
```



 

 
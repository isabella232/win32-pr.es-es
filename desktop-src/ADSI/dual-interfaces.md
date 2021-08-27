---
title: Interfaces duales (ADSI)
description: Use interfaces COM para acceder a las propiedades y métodos de cualquier objeto ADSI del proveedor.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d1cf89ef07e573be8f59805034ff8c567e75fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884061"
---
# <a name="dual-interfaces-adsi"></a>Interfaces duales (ADSI)

Use interfaces COM para acceder a las propiedades y métodos de cualquier objeto ADSI del proveedor. Una propiedad de solo lectura se asigna a una entrada de interfaz con el formato **get \_ &lt; PropertyName &gt;**. Una propiedad de lectura y escritura se asigna a dos entradas de interfaz con el formato **get \_ &lt; PropertyName &gt;** y **put \_ &lt; PropertyName &gt;**.

Todos los métodos de una interfaz COM deben:

-   Devuelve un valor HRESULT para indicar que se ha hecho correctamente o no. El **tipo HRESULT** se describe en la especificación COM.
-   En las llamadas **a QueryInterface**, devuelve **E \_ NOINTERFACE** para las interfaces sin implementar.
-   Devuelve **E \_ NOTIMPL para** los métodos no implementados en interfaces que se implementan de otro modo.
-   Devuelve **E ADS PROPERTY NOT SUPPORTED \_ \_ \_ \_ para** las propiedades de interfaz que no se admiten.

Para conservar la compatibilidad con los controladores de Automation, todos los parámetros y tipos de valor devuelto deben estar dentro del subconjunto definido por el tipo de datos VARIANT de Automation. Para más información, consulte **VARIANT** y **VARIANTARG** en Platform Software Development Kit (SDK).

Un proveedor Active Directory objeto puede exponer interfaces que usan tipos de datos distintos de los del **subconjunto VARIANT.** Sin embargo, los controladores de Automation Visual Basic no pueden llamar a esas interfaces. La mayoría de las interfaces de proveedor ADSI se derivan de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) y se pueden usar como punteros de interfaz **IDispatch.** Sin embargo, las interfaces [**ADSI IDirectoryObject,**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)e [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) no se derivan de **IDispatch.**

 

 

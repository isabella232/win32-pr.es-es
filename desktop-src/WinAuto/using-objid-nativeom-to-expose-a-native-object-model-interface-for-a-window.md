---
title: Uso de OBJID \_ NATIVEOM para exponer una interfaz nativa para una ventana
description: Esta técnica permite a los clientes obtener un objeto personalizado para una ventana. Los servidores pueden usarlo para exponer un puntero a un objeto de documento personalizado para una ventana.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed99db4641235ceee57688865710c19a41f0a517d70d4601d138150cb88dd470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098095"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Uso de OBJID \_ NATIVEOM para exponer una interfaz nativa para una ventana

Esta técnica permite a los clientes obtener un objeto personalizado para una ventana. Los servidores pueden usarlo para exponer un puntero a un objeto de documento personalizado para una ventana.

**Para exponer una interfaz de modelo de objetos nativa para una ventana (servidores)**

1.  Controle [**el mensaje WM \_ GETOBJECT**](wm-getobject.md) en el procedimiento de ventana. Cuando el *valor de lParam* es [**OBJID \_ NATIVEOM,**](object-identifiers.md)devuelve un puntero de interfaz al objeto personalizado [**mediante LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).
2.  Libere el puntero de interfaz después de llamar [**a LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), si procede. Para obtener más información, **vea LresultFromObject**.

Los clientes pueden obtener un puntero a este objeto personalizado.

**Para obtener un puntero para un objeto personalizado para una ventana (clientes)**

-   Llame [**a AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y pase [**OBJID \_ NATIVEOM**](object-identifiers.md) como segundo parámetro.

Tenga en cuenta los siguientes problemas para esta técnica:

-   Esta técnica es similar a devolver un puntero de interfaz [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) excepto para el identificador de objeto utilizado y el hecho de que [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) devuelve un objeto personalizado en lugar de **IAccessible**.
-   Es posible que los desarrolladores de servidores necesiten publicar información que permita a los clientes identificar de forma única el **HWND** para que puedan encontrarlo antes de llamar a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) en su identificador de ventana.
-   No implemente la [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto personalizado que se devuelve. Si lo hace, OLEACC lo tratará como un **IAccessible** estándar y puede impedir que se usen las interfaces personalizadas.
-   Para poder usarse en todos los procesos, es posible que las interfaces del objeto devuelto deban registrarse con el Modelo de objetos componentes (COM).

Esta técnica es compatible con varios Microsoft Office componentes. Para obtener más información, [**vea AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

 

 





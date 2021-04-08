---
title: Usar QueryService para recuperar una interfaz nativa para un objeto IAccessible
description: Los desarrolladores de servidores pueden utilizar esta técnica para exponer un puntero a un nodo de documento personalizado para un objeto IAccessible. Se supone que ya se exponen objetos IAccessible. Esta técnica permite a los clientes obtener un objeto personalizado de un objeto IAccessible.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078048"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Usar QueryService para recuperar una interfaz nativa para un objeto IAccessible

Los desarrolladores de servidores pueden utilizar esta técnica para exponer un puntero a un nodo de documento personalizado para un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Se supone que ya se exponen objetos **IAccessible** . Esta técnica permite a los clientes obtener un objeto personalizado de un objeto **IAccessible** .

**Para exponer un modelo de objetos nativo para un IAccessible (servidores)**

1.  Agregue compatibilidad para la interfaz **IServiceProvider** en el objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Defina un GUID que represente la funcionalidad de obtener la interfaz personalizada de los objetos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Esto se denomina identificador de servicio. Puede usar GUIDGEN.EXE para generar un identificador de servicio o reutilizar el identificador de interfaz si tiene una interfaz personalizada.
3.  Implemente el método **IServiceProvider:: QueryService** para que devuelva un puntero a la interfaz personalizada cuando se le llame con el identificador de servicio definido anteriormente en este procedimiento. **QueryService** debe devolver **null** para todos los demás valores de ID. de servicio.
4.  Publique el identificador de servicio para que los clientes puedan usarlo.

Los clientes pueden usar esta funcionalidad para obtener un puntero al objeto personalizado a partir de un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

**Para obtener un puntero a un objeto personalizado de un IAccessible (clientes)**

1.  Llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID \_ IServiceProvider) en un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para obtener un puntero de interfaz **IServiceProvider** .
2.  Llame a **IServiceProvider:: QueryService** con el identificador de servicio publicado para obtener un puntero al objeto personalizado para el [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
3.  Libere la interfaz **IServiceProvider** si ya no se necesita.

Para que se pueda usar en todos los procesos, es posible que los servidores deban registrar la interfaz devuelta con el modelo de objetos componentes (COM).

Microsoft Internet Explorer 4,0 y versiones posteriores utilizan esta técnica. Permite a los clientes obtener un puntero de interfaz **IHTMLElement2** que se corresponda con un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

 

 
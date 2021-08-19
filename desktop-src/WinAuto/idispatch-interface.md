---
title: Interfaz iDispatch y accesibilidad
description: La interfaz IDispatch se diseñó inicialmente para admitir Automation.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710fb0bc8142dfa863967114d3841506c220b3c058db042b867607ffe56cd5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052713"
---
# <a name="idispatch-interface-and-accessibility"></a>Interfaz iDispatch y accesibilidad

La [**interfaz IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) se diseñó inicialmente para admitir Automation. Proporciona un mecanismo de enlace en tiempo de entrega para obtener acceso y recuperar información sobre los métodos y propiedades de un objeto. Anteriormente, los desarrolladores de servidores tenían que implementar las interfaces **IDispatch** e [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para sus objetos accesibles. es decir, tenían que proporcionar una [interfaz dual.](dual-interfaces--iaccessible-and-idispatch.md) Con Microsoft Active Accessibility 2.0, los servidores pueden devolver **E \_ NOTIMPL** desde los métodos **IDispatch** y Microsoft Active Accessibility implementarán la **interfaz IAccessible** para ellos.

Además de los métodos heredados de [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)los desarrolladores de servidores deben implementar los métodos siguientes dentro de la definición de clase de cada objeto que se expone:

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) devuelve el número de descripciones de tipo para el objeto . Para los objetos que [**admiten IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), el recuento de información de tipos siempre es uno.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) recupera una descripción de la interfaz programable del objeto.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) asigna el nombre de un método o propiedad a **un DISPID**, que se usa más adelante para invocar el método o la propiedad .
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) llama a uno de los métodos del objeto o obtiene o establece una de sus propiedades.

 

 
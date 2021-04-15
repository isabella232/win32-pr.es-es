---
title: Interfaz IDispatch y accesibilidad
description: La interfaz IDispatch se diseñó inicialmente para admitir la automatización.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641ca3e4cc18b96441aefbbc46231e3f7753a94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665827"
---
# <a name="idispatch-interface-and-accessibility"></a>Interfaz IDispatch y accesibilidad

La interfaz [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) se diseñó inicialmente para admitir la automatización. Proporciona un mecanismo de enlace en tiempo de ejecución para obtener acceso y recuperar información sobre los métodos y propiedades de un objeto. Anteriormente, los desarrolladores de servidor tenían que implementar las interfaces **IDispatch** y [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para sus objetos accesibles. es decir, tenían que proporcionar una [interfaz dual](dual-interfaces--iaccessible-and-idispatch.md). Con Microsoft Active Accessibility 2,0, los servidores pueden devolver **E \_ NOTIMPL** de métodos **IDispatch** y Microsoft Active Accessibility implementará la interfaz **IAccessible** para ellos.

Además de los métodos heredados de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), los desarrolladores de servidor deben implementar los siguientes métodos en la definición de clase de cada objeto expuesto:

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) devuelve el número de descripciones de tipo para el objeto. En el caso de los objetos que admiten [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), el recuento de información de tipos siempre es uno.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) recupera una descripción de la interfaz programable del objeto.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) asigna el nombre de un método o propiedad a un **DISPID**, que se usa posteriormente para invocar el método o la propiedad.
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) llama a uno de los métodos del objeto u obtiene o establece una de sus propiedades.

 

 
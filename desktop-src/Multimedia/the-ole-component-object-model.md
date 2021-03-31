---
title: Modelo de objetos de componentes OLE
description: Modelo de objetos de componentes OLE
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "103995726"
---
# <a name="the-ole-component-object-model"></a>Modelo de objetos de componentes OLE

Los objetos utilizados por la biblioteca AVIFile forman parte del modelo de objetos de componentes OLE. Principalmente, esto significa que comparten ciertos métodos que facilitan el trabajo con y los valores que devuelven son comunes a la mayoría de los métodos de interfaz OLE.

El modelo de objetos de componentes OLE de los controladores de archivos y secuencias utiliza la interfaz OLE **IClassFactory** para crear instancias de su clase de objeto. Como objetos de componente, implementan la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , que consta de los métodos [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)), [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)y [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . La interfaz **IUnknown** permite a una aplicación obtener punteros a otras interfaces admitidas por el mismo objeto.

Puede determinar si un objeto admite una interfaz concreta mediante el método **QueryInterface** . Si un objeto admite una interfaz especificada, **QueryInterface** devuelve un puntero a esa interfaz.

Puede aumentar y disminuir el recuento de referencias asociado a un objeto mediante los métodos [**AddRef**](/previous-versions//dd757100(v=vs.85)) y [**Release**](/previous-versions//dd757102(v=vs.85)) . El recuento de referencias permite que varios clientes accedan a un objeto. Cuando la primera aplicación usa un objeto, su recuento de referencias se establece en 1. Posteriormente, las aplicaciones usan el método **AddRef** para incrementar el recuento y permitir que el objeto realice un seguimiento del número de veces que se tiene acceso a él.

Cuando una aplicación se realiza mediante un objeto, llama al método **Release** para reducir el recuento de referencias. Cuando el recuento de referencias es cero, el objeto ya no es necesario y **Release** libera todos los recursos que utiliza y destruye el objeto. Dado que un objeto utiliza recursos internos de forma transparente para la aplicación, el objeto es responsable de liberarlos. Por ejemplo, un controlador de archivos podría necesitar cerrar archivos de disco abiertos y la memoria de búfer libre cuando se lancen.

La mayoría de los métodos de interfaz OLE devuelven los identificadores de resultados que se definen mediante el tipo de datos **HRESULT** . Este tipo de datos se compone de un código de gravedad, información contextual, un código de instalación y un código de estado. Un identificador de resultado devuelto que indica que Success tiene el valor cero. Un valor distinto de cero indica un error y el miembro de código de estado del identificador de resultado devuelto proporciona una base para la interpretación adicional. Para obtener más información sobre los identificadores de resultados devueltos de OLE, vea la *Referencia del programador de OLE*.

 

 
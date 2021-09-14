---
title: El modelo de objetos de componente OLE
description: El modelo de objetos de componente OLE
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260671"
---
# <a name="the-ole-component-object-model"></a>El modelo de objetos de componente OLE

Los objetos utilizados por la biblioteca AVIFile forman parte del modelo de objetos de componente OLE. Principalmente, esto significa que comparten determinados métodos que facilitan el trabajo con ellos, y los valores que devuelven son comunes a la mayoría de los métodos de interfaz OLE.

El modelo de objetos de componente OLE de los controladores de archivos y secuencias usa la interfaz OLE **IClassFactory** para crear instancias de su clase de objeto. Como objetos de componente, implementan la [interfaz IUnknown,](/windows/win32/api/unknwn/nn-unknwn-iunknown) que consta de los métodos [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)), [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)y [**AddRef.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) La **interfaz IUnknown** permite a una aplicación obtener punteros a otras interfaces compatibles con el mismo objeto.

Puede determinar si un objeto admite una interfaz específica mediante el **método QueryInterface.** Si un objeto admite una interfaz especificada, **QueryInterface** devuelve un puntero a esa interfaz.

Puede incrementar y disminuir el recuento de referencias asociado a un objeto mediante los [**métodos AddRef**](/previous-versions//dd757100(v=vs.85)) [**y Release.**](/previous-versions//dd757102(v=vs.85)) El recuento de referencias permite que varios clientes accedan a un objeto . Cuando la primera aplicación usa un objeto, su recuento de referencias se establece en 1. Las aplicaciones usan posteriormente **el método AddRef** para incrementar el recuento para permitir que el objeto realice un seguimiento del número de veces que se accede a él.

Cuando una aplicación se completa con un objeto , llama al **método Release** para disminuir el recuento de referencias. Cuando el recuento de referencias es cero, el objeto ya no es necesario y **Release** libera los recursos que usa y destruye el objeto. Dado que un objeto usa recursos internos transparentes para la aplicación, el objeto es responsable de liberarlos. Por ejemplo, es posible que un controlador de archivos tenga que cerrar los archivos de disco abiertos y liberar memoria de búfer cuando se libera.

La mayoría de los métodos de interfaz OLE devuelven identificadores de resultados definidos mediante el tipo de datos **HRESULT.** Este tipo de datos está hecho de un código de gravedad, información contextual, un código de instalación y un código de estado. Un identificador de resultado devuelto que indica que la correcta tiene el valor cero. Un valor distinto de cero indica un error y el miembro de código de estado del identificador de resultado devuelto proporciona una base para una interpretación adicional. Para obtener información adicional sobre los identificadores de resultados devueltos de OLE, vea *ole programmer's Reference*.

 

 
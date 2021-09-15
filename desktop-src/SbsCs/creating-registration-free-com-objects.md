---
description: Los contextos de activación permiten usar objetos COM sin necesidad de que se registren.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Crear Registration-Free objetos COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271663"
---
# <a name="creating-registration-free-com-objects"></a>Crear Registration-Free objetos COM

Los contextos de activación permiten usar objetos COM sin necesidad de que se registren. Esto permite que la aplicación tenga varios componentes con funcionalidades diferentes en función de su versión en lugar de su información del Registro. Varios componentes pueden exponer el mismo objeto COM con el mismo GUID, pero tienen una funcionalidad diferente basada en la versión.

Cuando una aplicación solicita un GUID de [**CLSIDFromProgID,**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)COM busca primero la asignación de progid a CLSID en el contexto de activación activo. Cuando una aplicación usa [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un puntero de interfaz de instancia, COM busca en el contexto de activación activo para encontrar qué DLL hospedará el CLSID. Si el contexto de activación no contiene la información necesaria, COM busca la información en el Registro mediante el método habitual.

Tenga en cuenta que, dado que los contextos de activación son por subproceso, COM serializa el contexto de activación del subproceso de creación en el subproceso host y lo activa antes de llamar a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) en el subproceso host. Esta funcionalidad ya está presente en Windows, no es necesario que el código de cliente haga nada para implementar esto.

Los componentes hospedados pueden exportar clases COM sin pasar por el Registro. Varios componentes pueden exponer el mismo ProgID para distintos objetos COM y la aplicación de hospedaje solo debe encontrar el contexto de activación adecuado y, a continuación, usar [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener los punteros de interfaz del objeto hospedado.

 

 

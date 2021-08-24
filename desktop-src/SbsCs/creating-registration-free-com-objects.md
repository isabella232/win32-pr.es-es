---
description: Los contextos de activación permiten usar objetos COM sin necesidad de que se registren.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Crear Registration-Free objetos COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d5a6c8160eaf15eba4eb799123e0e79d126ccd94b1d4a7a6d332bdb27dd51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142368"
---
# <a name="creating-registration-free-com-objects"></a>Crear Registration-Free objetos COM

Los contextos de activación permiten usar objetos COM sin necesidad de que se registren. Esto permite que la aplicación tenga varios componentes con funcionalidades diferentes en función de su versión en lugar de su información del Registro. Varios componentes pueden exponer el mismo objeto COM con el mismo GUID, pero tienen funcionalidades diferentes basadas en la versión.

Cuando una aplicación solicita un GUID de [**CLSIDFromProgID,**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)COM busca primero la asignación de progid a CLSID en el contexto de activación activo. Cuando una aplicación usa [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un puntero de interfaz de instancia, COM busca en el contexto de activación activo para encontrar qué DLL hospedará el CLSID. Si el contexto de activación no contiene la información necesaria, COM busca la información en el Registro mediante el método habitual.

Tenga en cuenta que, dado que los contextos de activación son por subproceso, COM serializa el contexto de activación del subproceso de creación en el subproceso host y lo activa antes de llamar a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) en el subproceso host. Esta funcionalidad ya está presente en Windows, no es necesario que el código de cliente haga nada para implementar esto.

Los componentes hospedados pueden exportar clases COM sin pasar por el Registro. Varios componentes pueden exponer el mismo ProgID para diferentes objetos COM, y la aplicación de hospedaje solo debe encontrar el contexto de activación adecuado y, a continuación, usar [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener los punteros de interfaz del objeto hospedado.

 

 

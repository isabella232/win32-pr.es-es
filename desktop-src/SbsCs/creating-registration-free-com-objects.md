---
description: Los contextos de activación permiten usar objetos COM sin necesidad de que se registren.
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: Crear Registration-Free objetos COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648469"
---
# <a name="creating-registration-free-com-objects"></a>Crear Registration-Free objetos COM

Los contextos de activación permiten usar objetos COM sin necesidad de que se registren. Esto permite que la aplicación tenga varios componentes con funcionalidad diferente en función de su versión en lugar de la información del registro. Varios componentes pueden exponer el mismo objeto COM con el mismo GUID, pero tienen una funcionalidad diferente en función de la versión.

Cuando una aplicación solicita un GUID de [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), com busca primero la asignación desde ProgID a CLSID en el contexto de activación activo. Cuando una aplicación usa [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener un puntero de interfaz de instancia, com busca en el contexto de activación activo para encontrar qué dll hospedará el CLSID. Si el contexto de activación no contiene la información necesaria, COM busca la información en el registro con el método habitual.

Tenga en cuenta que, dado que los contextos de activación son por subproceso, COM calcula las referencias del contexto de activación del subproceso de creación en el subproceso de host y lo activa antes de llamar a [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) en el subproceso de host. Esta funcionalidad ya está presente en Windows, no es necesario que el código de cliente haga nada para implementar esto.

Los componentes hospedados pueden exportar las clases COM sin pasar por el registro. Varios componentes pueden exponer el mismo ProgID para objetos COM diferentes y la aplicación de hospedaje solo debe encontrar el contexto de activación adecuado y, a continuación, usar [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para obtener los punteros de interfaz del objeto hospedado.

 

 

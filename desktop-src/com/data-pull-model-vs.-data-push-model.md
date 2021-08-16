---
title: Data-Pull modelo y Data-Push modelo
description: Data-Pull modelo y Data-Push modelo
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab89f61301f9116a7e826f1965bd54f75004a3a90af8c9d1a1bc13acb1fc9c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048453"
---
# <a name="data-pull-model-and-data-push-model"></a>Data-Pull modelo y Data-Push modelo

Un cliente de un moniker asincrónico puede elegir entre un modelo de extracción de datos y de inserción de datos para impulsar una operación [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) asincrónica y recibir notificaciones asincrónicas. En el modelo de extracción de datos, el cliente dirige la operación de enlace y el moniker proporciona datos al cliente solo cuando se lee. En otras palabras, después de la primera llamada a [**IBindStatusCallback::OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), el moniker no proporciona ningún dato al cliente a menos que el cliente haya consumido todos los datos que ya están disponibles.

Dado que los datos se descargan solo cuando se solicitan, los clientes que eligen el modelo de extracción de datos deben asegurarse de leer estos datos de forma oportuna. En el caso de las descargas de Internet con [monikers](url-monikers.md)de dirección URL, la operación de enlace puede producir un error si un cliente espera demasiado tiempo antes de solicitar más datos.

En el modelo de inserción de datos, el moniker impulsa la operación de enlace asincrónica y notifica continuamente al cliente cada vez que hay nuevos datos disponibles. El cliente puede elegir si leer los datos en cualquier momento durante la operación de enlace, pero el moniker llevará la operación de enlace a la finalización, independientemente de.

Además, debe recordar seguir las reglas COM para la asignación de memoria al usar monikers asincrónicos, específicamente los siguientes:

-   Cada vez que una llamada de función o interfaz COM devuelve un búfer (cadena u otro) a su cliente, el cliente es responsable de liberar la memoria mediante una llamada a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).
-   Cada vez que una interfaz o función COM requiere un búfer de su cliente, el cliente debe asignar ese búfer mediante [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) y el destinatario debe liberarlo.

Asegúrese de seguir estas reglas al asignar cadenas o búferes que se pasan a monikers asincrónicos y recuerde liberar memoria devuelta por monikers asincrónicos. Consulte [Administración de la asignación de](the-com-library.md) memoria y temas relacionados para obtener detalles completos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 
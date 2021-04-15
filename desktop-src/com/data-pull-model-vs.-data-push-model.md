---
title: Modelo de Data-Pull y modelo de Data-Push
description: Modelo de Data-Pull y modelo de Data-Push
ms.assetid: ba0e8532-9c7b-4e15-9c27-8205d738fc4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f6607e9b466c439859a99b857e7ce3fe6d8acd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421489"
---
# <a name="data-pull-model-and-data-push-model"></a>Modelo de Data-Pull y modelo de Data-Push

Un cliente de un moniker asincrónico puede elegir entre un modelo de extracción de datos y de inserción de datos para impulsar una operación [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) asincrónica y recibir notificaciones asincrónicas. En el modelo de extracción de datos, el cliente controla la operación de enlace y el moniker proporciona datos al cliente solo a medida que se leen. En otras palabras, después de la primera llamada a [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)), el moniker no proporciona ningún dato al cliente a menos que el cliente haya consumido todos los datos que ya están disponibles.

Dado que los datos se descargan solo cuando se solicita, los clientes que eligen el modelo de extracción de datos deben asegurarse de leer estos datos a tiempo. En el caso de las descargas de Internet con [monikers URL](url-monikers.md), se puede producir un error en la operación de enlace si un cliente espera demasiado tiempo antes de solicitar más datos.

En el modelo de extracción de datos, el moniker controla la operación de enlace asincrónica y notifica continuamente al cliente cada vez que haya nuevos datos disponibles. El cliente puede elegir si desea leer los datos en cualquier momento durante la operación de enlace, pero el moniker hará que la operación de enlace se complete sin tener en consideración.

Además, debe recordar seguir las reglas COM para la asignación de memoria cuando se usan monikers asincrónicos, específicamente los siguientes:

-   Siempre que una llamada de función o interfaz COM devuelve un búfer (cadena u otro) a su cliente, el cliente es responsable de liberar la memoria mediante una llamada a [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).
-   Siempre que una interfaz o función COM requiere un búfer de su cliente, el cliente debe asignar ese búfer mediante [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) y el destinatario debe liberarlo.

Asegúrese de seguir estas reglas al asignar las cadenas o los búferes que se pasan a los monikers asincrónicos y recuerde liberar la memoria devuelta por los monikers asincrónicos. Consulte [Administración](the-com-library.md) de la asignación de memoria y temas relacionados para obtener detalles completos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 
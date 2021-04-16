---
title: Sincronización de devolución de llamada
description: Sincronización de devolución de llamada
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714470"
---
# <a name="callback-synchronization"></a>Sincronización de devolución de llamada

La API de [WinInet](/windows/desktop/WinInet/portal) asincrónica (utilizada para los protocolos más comunes) deja la sincronización del mecanismo de devolución de llamada y la aplicación que realiza la llamada como un ejercicio para el cliente. Esto es intencionado porque permite el mayor grado de flexibilidad. Los protocolos predeterminados y la implementación de moniker de dirección URL realizan esta sincronización y garantizan que las aplicaciones de un solo subproceso y de subprocesamiento controlado nunca tienen que tratar con la contención de estilo de subproceso libre. Es decir, solo se llama a las interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) y [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) del cliente en los subprocesos correspondientes. Esta característica es transparente para el usuario de la dirección URL mMoniker siempre que cada subproceso que llama a [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) y [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) tiene una cola de mensajes.

La especificación de moniker asincrónico requiere un control más preciso sobre la priorización y la administración de las descargas que se permite en WinSock o WinInet. En consecuencia, un moniker de dirección URL administra todas las descargas de cualquier subproceso del llamador determinado, usando (como parte de su sincronización) un esquema de prioridad basado en la especificación [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers de URL](url-monikers.md)
</dt> </dl>

 

 
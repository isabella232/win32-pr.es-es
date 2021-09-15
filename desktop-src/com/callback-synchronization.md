---
title: Sincronización de devolución de llamada
description: Sincronización de devolución de llamada
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466983"
---
# <a name="callback-synchronization"></a>Sincronización de devolución de llamada

La [API asincrónica de WinInet](/windows/desktop/WinInet/portal) (que se usa para los protocolos más comunes) deja la sincronización del mecanismo de devolución de llamada y la aplicación de llamada como un ejercicio para el cliente. Esto es intencionado porque permite el mayor grado de flexibilidad. Los protocolos predeterminados y la implementación del moniker de dirección URL realizan esta sincronización y garantizan que las aplicaciones de un solo subproceso y subprocesos de apartamento nunca tienen que tratar con la contención de estilo de subproceso libre. Es decir, solo se llama a las interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) del cliente en sus subprocesos adecuados. Esta característica es transparente para el usuario de la dirección URL mMoniker siempre que cada subproceso que llame a [**IMoniker::BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) tenga una cola de mensajes.

La especificación del moniker asincrónico requiere un control más preciso sobre la priorización y la administración de las descargas de las permitidas por WinSock o WinInet. En consecuencia, un moniker de dirección URL administra todas las descargas para el subproceso de un llamador determinado, usando (como parte de su sincronización) un esquema de prioridad basado en la especificación [**IBinding.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 
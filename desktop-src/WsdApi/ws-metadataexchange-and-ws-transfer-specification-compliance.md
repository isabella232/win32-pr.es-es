---
description: Antes de agosto de 2006, WS-MetadataExchange definió su propio método de intercambio de metadatos Get, que usaba Devices Profile for Web Services (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: WS-MetadataExchange y cumplimiento de WS-Transfer especificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bec29d96b4ba3671f176349a56b891cd4d642762670fd16cf582da53208c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793975"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>WS-MetadataExchange y cumplimiento de WS-Transfer especificación

Antes de agosto de 2006, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) definió su propio método de intercambio de metadatos [Get,](get--metadata-exchange--http-request-and-message.md) que usaba [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). La WS-MetadataExchange de especificación 1.1 reemplazó este método por el método Get definido en WS-Transfer especificación.

En el modelo actual, WS-Transfer proporciona el [método Get](get--metadata-exchange--http-request-and-message.md) y no hace referencia al tipo del cuerpo. WS-MetadataExchange describe el formato del cuerpo y un mecanismo para empaquetar varios fragmentos de metadatos en una única respuesta, y DPWS describe fragmentos específicos de metadatos que un servicio debe incluir en una respuesta de metadatos.

WSDAPI no admite totalmente la especificación WS-Transfer datos. Dado que solo [se requiere](get--metadata-exchange--http-request-and-message.md) el método Get para los dispositivos, no se WS-Transfer ninguna otra parte de la aplicación. Además, WSDAPI no implementa el método GetMetadata opcional descrito en WS-MetadataExchange.

 

 




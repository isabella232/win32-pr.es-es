---
description: Antes del 2006 de agosto, WS-MetadataExchange definido su propio método get Metadata Exchange, que se usó en el perfil de dispositivos para servicios web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Compatibilidad de la especificación de WS-MetadataExchange y WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ecad5224256f35b2157088ce091e8bd5751c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155801"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>Compatibilidad de la especificación de WS-MetadataExchange y WS-Transfer

Antes del 2006 de agosto de [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) , se definió su propio método [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange, que se usaba en el [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). La versión 1,1 de la especificación de WS-MetadataExchange ha reemplazado este método por el método get definido en la especificación de WS-Transfer.

En el modelo actual, WS-Transfer proporciona el método [Get](get--metadata-exchange--http-request-and-message.md) y no hace referencia al tipo del cuerpo. WS-MetadataExchange describe el formato del cuerpo y un mecanismo para empaquetar varios fragmentos de metadatos en una sola respuesta, y DPWS describe partes específicas de los metadatos que un servicio debe incluir en una respuesta de metadatos.

WSDAPI no es totalmente compatible con la especificación WS-Transfer. Dado que solo se requiere el método [Get](get--metadata-exchange--http-request-and-message.md) para los dispositivos, no se han implementado otras partes de WS-Transfer. Además, WSDAPI no implementa el método GetMetadata opcional que se describe en WS-MetadataExchange.

 

 




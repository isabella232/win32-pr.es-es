---
description: En el diagrama siguiente se muestran los objetos principales implicados en los controles de blobs en conferencias TAPI 3. Las interfaces mostradas se hipervínculon a las páginas de referencia pertinentes.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controles de blobs en conferencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068772"
---
# <a name="conference-blob-controls"></a>Controles de blobs en conferencias

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

En el diagrama siguiente se muestran los objetos principales implicados en los controles de blobs en conferencias TAPI 3. Las interfaces mostradas se hipervínculon a las páginas de referencia pertinentes.

![interfaces y controles de blobs de conferencia](images/rendblob.png)

El blob en conferencias contiene información específica del proveedor sobre un objeto de conferencia. Para obtener un puntero al blob de interfaz [**ITConferenceBlob,**](itconferenceblob.md) se usa QueryInterface en [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference). La **interfaz ITConferenceBlob proporciona métodos** para la manipulación básica de un blob de conferencia genérico. Una aplicación que usa blobs de conferencia que no son SDP debe implementar sus propios métodos para la manipulación de detalles.

Rendezvous proporciona la [**interfaz ITSdp**](itsdp.md) para manipular blobs en conferencias de SDP. SDP es un protocolo para describir sesiones multimedia y su información de programación relacionada. Para obtener información adicional sobre el protocolo SDP, busque Internet Engineering Task Force (IETF) RFC 2327 con el título "SDP: Protocolo de descripción de sesión". Si la **interfaz ITSDP** existe para un blob de conferencia determinado, puede obtener un puntero a él mediante una **queryinterface** en [**ITConferenceBlob**](itconferenceblob.md).

En el caso de los blobs en conferencias de SDP, las interfaces [**ITTimeCollection,**](ittimecollection.md) [**ITTime,**](ittime.md) [**ITMediaCollection**](itmediacollection.md)e [**ITMedia**](itmedia.md) permiten un control detallado de las características multimedia y el tiempo de conferencia de SDP.

 

 




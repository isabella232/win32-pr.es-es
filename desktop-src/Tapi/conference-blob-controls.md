---
description: En el diagrama siguiente se muestran los objetos principales implicados en los controles de BLOB de la Conferencia TAPI 3. Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controles de BLOB de conferencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542990"
---
# <a name="conference-blob-controls"></a>Controles de BLOB de conferencia

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

En el diagrama siguiente se muestran los objetos principales implicados en los controles de BLOB de la Conferencia TAPI 3. Las interfaces que se muestran se hipervinculan en las páginas de referencia pertinentes.

![interfaces y controles de blobs en conferencias](images/rendblob.png)

El BLOB de la Conferencia contiene información específica del proveedor en un objeto de conferencia. Un puntero al BLOB de la interfaz [**ITConferenceBlob**](itconferenceblob.md) se obtiene mediante QueryInterface en [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference). La interfaz **ITConferenceBlob** proporciona métodos para la manipulación básica de un BLOB de conferencia genérico. Una aplicación que usa blobs de conferencias no SDP debe implementar sus propios métodos para la manipulación detallada.

Rendezvous proporciona la interfaz [**ITSdp**](itsdp.md) para manipular los blobs de la Conferencia SDP. SDP es un protocolo para describir las sesiones multimedia y su información de programación relacionada. Para obtener información adicional sobre el protocolo SDP, busque el RFC 2327 de Internet Engineering Task Force (IETF) titulado "SDP: Protocolo de descripción de la sesión". Si la interfaz **ITSDP** existe para un BLOB de conferencia determinado, puede obtener un puntero a ella mediante **QueryInterface** en [**ITConferenceBlob**](itconferenceblob.md).

En el caso de los blobs de la Conferencia SDP, las interfaces [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)y [**ITMedia**](itmedia.md) permiten el control detallado del tiempo de conferencia SDP y de las características multimedia.

 

 




---
title: EC_WMT_INDEX_EVENT (Windows SDK de Formato multimedia 11)
description: EVENTO \_ DE ÍNDICE WMT DE \_ \_ EC
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Windows SDK de formato multimedia, EC_WMT_INDEX_EVENT
- DirectShow,EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Formato de sistemas avanzados (ASF),EC_WMT_INDEX_EVENT
- ASF (formato de sistemas avanzados),EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360590"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (Windows SDK de Formato multimedia 11)

Enviado por el SDK Windows Media Format cuando una aplicación usa ASF Writer para indexar Windows archivos de vídeo multimedia.

Parámetros

*lParam1*

Puede ser cualquiera de los siguientes **mensajes DE ESTADO \_ DE WMT.**



| Message              | Descripción                                     |
|----------------------|-------------------------------------------------|
| WMT \_ STARTED         | La indexación ha comenzado. *lParam2* es cero.          |
| WMT \_ CLOSED          | Se ha completado la indexación. *lParam2* es cero. |
| PROGRESO DEL \_ ÍNDICE WMT \_ | La indexación está en curso.                        |



 

*lParam2*

Si *lParam1* es WMT \_ CLOSED o WMT \_ STARTED, *lParam2* es cero. Si *lParam1* es WMT \_ INDEX \_ PROGRESS, *lParam2* es un **DWORD** que expresa la cantidad de progreso como porcentaje del tamaño total de descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DirectShow Referencia de QASF**](directshow-qasf-reference.md)
</dt> </dl>

 

 





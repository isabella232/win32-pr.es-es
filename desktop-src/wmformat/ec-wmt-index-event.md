---
title: EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)
description: '\_evento de \_ Índice \_ WMT de EC'
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- SDK de Windows Media Format, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Advanced Systems Format (ASF), EC_WMT_INDEX_EVENT
- ASF (formato de sistemas avanzados), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078699"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a>EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)

Lo envía el SDK de Windows Media Format cuando una aplicación utiliza el escritor ASF para indizar Windows Media Video archivos.

Parámetros

*lParam1*

Puede ser cualquiera de los siguientes mensajes **de \_ Estado de WMT** .



| Message              | Descripción                                     |
|----------------------|-------------------------------------------------|
| WMT \_ iniciado         | La indización ha comenzado. *lParam2* es cero.          |
| WMT \_ cerrado          | Se ha completado la indexación. *lParam2* es cero. |
| \_progreso del índice WMT \_ | La indexación está en curso.                        |



 

*lParam2*

Si *lParam1* es WMT \_ Closed o WMT \_ iniciado, entonces *lParam2* es cero. Si *lParam1* es \_ \_ el progreso del índice WMT, *lParam2* es un **valor DWORD** que expresa la cantidad de progreso como un porcentaje del tamaño total de la descarga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de QASF de DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 





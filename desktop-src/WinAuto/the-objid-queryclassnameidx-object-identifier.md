---
title: Identificador del objeto OBJID_QUERYCLASSNAMEIDX
description: Microsoft Active Accessibility usa el identificador de objeto de OBJID \_ QUERYCLASSNAMEIDX con el \_ mensaje de WM GETOBJECT para determinar la clase a la que pertenece un control común o un control de Windows estándar.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704577"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>Identificador de \_ objeto de QUERYCLASSNAMEIDX OBJID

Microsoft Active Accessibility usa el identificador de objeto de [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) con el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para determinar la clase a la que pertenece un control común o un control de Windows estándar. Un control responde a este mensaje devolviendo un valor que Microsoft Active Accessibility asigna al nombre de clase del control. Microsoft Active Accessibility usa esta información para proporcionar compatibilidad de accesibilidad para los controles estándar de Windows y los controles comunes.

Por lo general, solo los controles estándar de Windows y los controles comunes responden al identificador de objeto de [**\_ QUERYCLASSNAMEIDX OBJID**](object-identifiers.md) . Sin embargo, un control personalizado también puede responder si incluye la misma funcionalidad que un control estándar o común de Windows existente. Esto permite que el control personalizado sea compatible con uno de los objetos proxy estándar proporcionados por Microsoft Active Accessibility.

Para obtener más información, vea el [Apéndice F: valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 





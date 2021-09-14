---
title: Identificador OBJID_QUERYCLASSNAMEIDX objeto
description: Microsoft Active Accessibility usa el identificador de objeto OBJID QUERYCLASSNAMEIDX con el mensaje WM GETOBJECT para determinar la clase a la que pertenece un control Windows estándar o \_ \_ un control común.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070611"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>Identificador de objeto OBJID \_ QUERYCLASSNAMEIDX

Microsoft Active Accessibility usa el identificador de objeto [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) con el mensaje [**WM \_ GETOBJECT**](wm-getobject.md) para determinar la clase a la que pertenece un control Windows estándar o un control común. Un control responde a este mensaje devolviendo un valor que Microsoft Active Accessibility asigna al nombre de clase del control. Microsoft Active Accessibility esta información para proporcionar compatibilidad de accesibilidad para controles Windows estándar y controles comunes.

Por lo general, solo los controles Windows estándar y los controles comunes responden al identificador de objeto [**OBJID \_ QUERYCLASSNAMEIDX.**](object-identifiers.md) Sin embargo, un control personalizado también puede responder si incluye toda la misma funcionalidad que un control estándar Windows control o control común. Esto permite que el control personalizado sea compatible con uno de los objetos de proxy estándar proporcionados por Microsoft Active Accessibility.

Para obtener más información, [vea Apéndice F: Valores de identificador de objeto para OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 





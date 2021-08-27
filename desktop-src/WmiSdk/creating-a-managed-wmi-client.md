---
description: WMI no admite actualmente código administrado en WMI, pero se admite en MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Creación de un cliente WMI administrado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071525"
---
# <a name="creating-a-managed-wmi-client"></a>Creación de un cliente WMI administrado

La versión actual de WMI contiene el espacio de nombres System.Management, que expone una serie de API que interactúan con WMI. Sin embargo, no se recomienda usar este espacio de nombres.

Si desea crear un cliente WMI administrado, se recomienda usar la infraestructura Windows administración administrada (MI). MI es la versión de próxima generación de WMI y contiene compatibilidad completa con código administrado. Para obtener más información, [vea How to Implement a Managed MI Client](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 

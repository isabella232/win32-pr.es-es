---
description: WMI no admite actualmente código administrado en WMI, pero sí se admite en MI.
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: Crear un cliente WMI administrado
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb1339347c4e15cd29ebf4d4e98e5a8b61a24e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706174"
---
# <a name="creating-a-managed-wmi-client"></a>Crear un cliente WMI administrado

La versión actual de WMI contiene el espacio de nombres System. Management, que expone una serie de API que interactúan con WMI. Sin embargo, no se recomienda usar este espacio de nombres.

Si desea crear un cliente WMI administrado, se recomienda que use la infraestructura de administración de Windows (MI). MI es la versión de la próxima generación de WMI y contiene compatibilidad total con el código administrado. Para obtener más información, vea [cómo implementar un cliente de mi administrado](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client).

 

 

---
description: Si una aplicación no quiere interferencias de eventos externos para una sesión de TAPI o del proveedor de servicios, debe proteger la llamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ee16dc0854c6502f1347a3aa676e709920555ad91a02190db001bd80b34824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080465"
---
# <a name="secure-a-session"></a>Proteger una sesión

Si una aplicación no quiere interferencias de eventos externos para una sesión de TAPI o del proveedor de servicios, debe proteger la llamada. Por ejemplo, en un entorno análogo, los tonos de espera de llamada pueden destruir una sesión de fax o módem en la llamada original.

Una aplicación puede proteger una llamada en el momento en que se realiza la llamada o después de que ya exista la llamada.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Consulte [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3.x:** Vea [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 

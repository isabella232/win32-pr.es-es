---
description: Si una aplicación no desea interferencias por parte de eventos externos para una sesión de TAPI o del proveedor de servicios, debe proteger la llamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474681"
---
# <a name="secure-a-session"></a>Proteger una sesión

Si una aplicación no desea interferencias por parte de eventos externos para una sesión de TAPI o del proveedor de servicios, debe proteger la llamada. Por ejemplo, en un entorno análogo, los tonos de espera de llamadas pueden destruir una sesión de fax o módem en la llamada original.

Una aplicación puede proteger una llamada en el momento en que se realiza la llamada o después de que la llamada ya exista.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Vea [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3.x:** Vea [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 

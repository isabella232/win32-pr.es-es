---
description: Si una aplicación no desea interferencias fuera de los eventos de una sesión de TAPI o del proveedor de servicios, debe proteger la llamada.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteger una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689546"
---
# <a name="secure-a-session"></a>Proteger una sesión

Si una aplicación no desea interferencias fuera de los eventos de una sesión de TAPI o del proveedor de servicios, debe proteger la llamada. Por ejemplo, en un entorno analógico, los tonos en espera pueden destruir una sesión de fax o módem en la llamada original.

Una aplicación puede proteger una llamada en el momento en que se realiza la llamada o después de que la llamada ya exista.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).

**TAPI 3. x:** Vea [**ITAddress:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).

 

 

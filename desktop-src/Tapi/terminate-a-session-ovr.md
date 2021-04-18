---
description: La finalización de la sesión puede provenir de una solicitud de usuario, de una desconexión remota por parte de la otra o de razones específicas de la aplicación.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Finalizar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688749"
---
# <a name="terminate-a-session"></a>Finalizar una sesión

La finalización de la sesión puede provenir de una solicitud de usuario, de una desconexión remota por parte de la otra o de razones específicas de la aplicación. Cuando finaliza una sesión, el [identificador de sesión](session-identifier-ovr.md) sigue siendo válido hasta que se libera específicamente y se puede usar para recopilar datos posteriores a la conexión.

La finalización de la sesión se completa desasignando y liberando los recursos asociados a la sesión. Si una sesión simplemente se quita o se desconecta pero no se liberan recursos, el resultado es una pérdida de memoria en la aplicación y posiblemente también en el proveedor de servicios.

**TAPI 2. x:** Vea [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).

**TAPI 3. x:** Vea [**ITBasicCallControl::D Ulta**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), realizar una versión com estándar en el puntero del objeto de llamada.

 

 

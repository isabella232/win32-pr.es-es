---
description: Utilice la función EventWriteTransfer cuando varios componentes deseen relacionar sus eventos en un escenario de seguimiento de un extremo a otro.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Escribir eventos relacionados en un proveedor basado en manifiestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543067"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Escribir eventos relacionados en un proveedor basado en manifiestos

Utilice la función [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) cuando varios componentes deseen relacionar sus eventos en un escenario de seguimiento de un extremo a otro. Por ejemplo, los componentes A, B y C realizan trabajo en una actividad relacionada y desean vincular todos los eventos relacionados con esa actividad.

ETW usa el almacenamiento local de subprocesos para que el identificador de actividad del componente anterior esté disponible para el componente siguiente. El componente recupera el identificador del componente anterior del almacenamiento local y establece el identificador de actividad relacionado en él. A continuación, el consumidor puede utilizar el identificador de actividad relacionado para recorrer la cadena de eventos de un componente al siguiente.

 

 




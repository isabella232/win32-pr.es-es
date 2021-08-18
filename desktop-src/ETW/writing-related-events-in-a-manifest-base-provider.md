---
description: Use la función EventWriteTransfer cuando varios componentes quieran relacionar sus eventos en un escenario de seguimiento de un extremo a otro.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Escribir eventos relacionados en un proveedor basado en manifiestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f6d09e7e95617b662c3530497b199925921ef9abfd4f3825a5ac799886f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015213"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Escribir eventos relacionados en un proveedor basado en manifiestos

Use la [**función EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) cuando varios componentes quieran relacionar sus eventos en un escenario de seguimiento de un extremo a otro. Por ejemplo, los componentes A, B y C realizan el trabajo en una actividad relacionada y desean vincular todos los eventos relacionados con esa actividad.

ETW usa el almacenamiento local de subprocesos para que el identificador de actividad del componente anterior esté disponible para el componente siguiente. El componente recupera el identificador del componente anterior del almacenamiento local y establece el identificador de actividad relacionado en él. A continuación, el consumidor puede usar el identificador de actividad relacionado para recorrer la cadena de los eventos de un componente al siguiente.

 

 




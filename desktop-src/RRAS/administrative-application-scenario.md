---
title: Escenario de aplicación administrativa
description: Las aplicaciones administrativas llaman a un subconjunto de funciones MGM relacionadas con la enumeración de entradas de reenvío de multidifusión (MFE) y estadísticas de MFE.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c8574a0e6ab85fe4e826a224377fa0de5de3851b7e31264b4c68c3c2fce56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791920"
---
# <a name="administrative-application-scenario"></a>Escenario de aplicación administrativa

Las aplicaciones administrativas llaman a un subconjunto de funciones MGM relacionadas con la enumeración de entradas de reenvío de multidifusión (MFE) y estadísticas de MFE. Una aplicación no necesita registrarse con el administrador de grupos de multidifusión para usar estas funciones (es decir, la aplicación no necesita un identificador).

## <a name="enumerating-mfes"></a>Enumeración de mfes

En la tabla siguiente se resume una serie de pasos en una interacción entre una aplicación administrativa y el administrador de grupos de multidifusión. En la primera columna se describen las acciones que realiza la aplicación administrativa y las respuestas de la aplicación administrativa al administrador de grupos de multidifusión. En la segunda columna se describen las respuestas del administrador de grupos de multidifusión a la aplicación administrativa. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.



| Acción de aplicación administrativa                                                                                                                                                                                      | Acción del administrador de grupos de multidifusión                                                                                                                                                                                                                                                              | Notas                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenga una o varias MFE mediante la [**función MgmGetFirstMfe.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)                                                                                                                                   | Devuelve tantas MFE como quepa en el búfer proporcionado por el cliente. Si no se puede devolver ninguna MFE en el búfer proporcionado, devuelva ERROR INSUFFICIENT BUFFER y el tamaño del búfer necesario para \_ \_ devolver un MFE.<br/>                                                              | Los clientes también pueden recuperar estadísticas MFE mediante las funciones estadísticas correspondientes, [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) y [**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats). |
| Si se recibe ERROR INSUFFICIENT BUFFER, llame de nuevo a la \_ \_ función [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) con un búfer del tamaño indicado.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Siga llamando a la función [**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) y proporcione como uno de los parámetros el último MFE devuelto por la llamada anterior a la [**función MgmGetFirstMfe.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) | Devuelve tantas MFE como quepa en el búfer proporcionado por el cliente. Si no se puede devolver ninguna MFE en el búfer proporcionado, devuelva ERROR INSUFFICIENT BUFFER y el tamaño del búfer necesario \_ \_ para un MFE.<br/> Devuelve EL ERROR \_ NO HAY MÁS ELEMENTOS cuando ya no quedan más \_ \_ MFE.<br/> |                                                                                                                                                                                                 |
| Continúe con la enumeración hasta que se reciba ERROR \_ NO \_ MORE \_ ITEMS.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Use las [**funciones MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) y [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) para recuperar un MFE específico o un conjunto específico de estadísticas MFE.

 

 

 






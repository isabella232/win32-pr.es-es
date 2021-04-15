---
title: Escenario de aplicación administrativa
description: Las aplicaciones administrativas llaman a un subconjunto de funciones MGM que están relacionadas con la enumeración de entradas de reenvío de multidifusión (MFEs) y estadísticas de MFE.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c7d69b88503f7a4af18f0ab4650923a2845f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676187"
---
# <a name="administrative-application-scenario"></a>Escenario de aplicación administrativa

Las aplicaciones administrativas llaman a un subconjunto de funciones MGM que están relacionadas con la enumeración de entradas de reenvío de multidifusión (MFEs) y estadísticas de MFE. No es necesario que una aplicación se registre con el administrador del grupo de multidifusión para usar estas funciones (es decir, la aplicación no necesita un identificador).

## <a name="enumerating-mfes"></a>Enumerar MFEs

En la tabla siguiente se resume una serie de pasos en una interacción entre una aplicación administrativa y el administrador del grupo de multidifusión. En la primera columna se describen las acciones que realiza la aplicación administrativa y las respuestas de la aplicación administrativa al administrador del grupo de multidifusión. En la segunda columna se describen las respuestas del administrador del grupo de multidifusión a la aplicación administrativa. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.



| Acción de aplicación administrativa                                                                                                                                                                                      | Acción del administrador del grupo de multidifusión                                                                                                                                                                                                                                                              | Notas                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtener uno o varios MFEs mediante la función [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) .                                                                                                                                   | Devuelve tantos MFEs como quepan en el búfer proporcionado por el cliente. Si no se puede devolver ningún MFEs en el búfer proporcionado, \_ se devuelve \_ un error de búfer insuficiente y el tamaño del búfer necesario para devolver una MFE.<br/>                                                              | Los clientes también pueden recuperar estadísticas de MFE mediante las funciones de estadísticas correspondientes, [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) y [**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats). |
| Si \_ \_ se recibe un error de búfer insuficiente, vuelva a llamar a la función [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) con un búfer con el tamaño indicado.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Continúe llamando a la función [**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) , proporcionando como uno de los parámetros el último MFE devuelto por la llamada anterior a la función [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) . | Devuelve tantos MFEs como quepan en el búfer proporcionado por el cliente. Si no se puede devolver ningún MFEs en el búfer proporcionado, \_ se devuelve \_ un error de búfer insuficiente y el tamaño del búfer necesario para una MFE.<br/> Devuelve el ERROR \_ no hay \_ más \_ elementos cuando no quedan más MFEs.<br/> |                                                                                                                                                                                                 |
| Continuar la enumeración hasta que \_ no \_ se reciba el error. no \_ se reciben más elementos.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Use las funciones [**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) y [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) para recuperar un MFE específico o un conjunto específico de estadísticas de MFE.

 

 

 






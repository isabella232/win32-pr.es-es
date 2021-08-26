---
title: Devoluciones de llamada de alertas de interfaz incorrectas
description: Una vez que el reenviador del kernel recibe datos de multidifusión de un origen específico en la interfaz incorrecta, notifica al administrador de grupos de multidifusión.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ac3354b1355cbcb1654b41a61ab046e74ec41b8dc716de6d50f7d9d52b18d94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024655"
---
# <a name="wrong-interface-alert-callbacks"></a>Devoluciones de llamada de alertas de interfaz incorrectas

Una vez que el reenviador del kernel recibe datos de multidifusión de un origen específico en la interfaz incorrecta, notifica al administrador de grupos de multidifusión. A continuación, el administrador de grupos de multidifusión invoca la devolución de llamada [**IF \_ \_ \_ CALLBACK**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) de PMGM WRONG al protocolo de enrutamiento que posee la interfaz en la que llegaron los datos incorrectamente.

> [!Note]  
> Esta devolución de llamada no está implementada actualmente en esta versión de la API de MGM.

 

 

 





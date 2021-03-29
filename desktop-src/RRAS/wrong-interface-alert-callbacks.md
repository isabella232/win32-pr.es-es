---
title: Devoluciones de llamada de alerta de interfaz errónea
description: Una vez que el reenviador de kernel recibe datos de multidifusión de un origen específico en la interfaz equivocada, se lo notifica al administrador del grupo de multidifusión.
ms.assetid: 7b20625e-286b-4c4f-8452-4d21563fd030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12906d836ca994e90347ea78cf22e50f8f2f00d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779447"
---
# <a name="wrong-interface-alert-callbacks"></a>Devoluciones de llamada de alerta de interfaz errónea

Una vez que el reenviador de kernel recibe datos de multidifusión de un origen específico en la interfaz equivocada, se lo notifica al administrador del grupo de multidifusión. A continuación, el administrador del grupo de multidifusión invoca el [**PMGM \_ incorrecto \_ si \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback) la devolución de llamada de devolución de llamada al Protocolo de enrutamiento que posee la interfaz en la que los datos llegaron incorrectamente.

> [!Note]  
> Esta devolución de llamada no está implementada actualmente en esta versión de la API MGM.

 

 

 





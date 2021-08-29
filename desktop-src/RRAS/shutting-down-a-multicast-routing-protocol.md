---
title: Apagar un protocolo de enrutamiento de multidifusión
description: En la tabla siguiente se resume una serie de pasos en una interacción de apagado entre el administrador de grupos de multidifusión y el protocolo de enrutamiento cuando se cierra el protocolo de enrutamiento.
ms.assetid: d868218d-7939-45d1-9e2f-3415c40f1a62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910b1097b21c75788cd802b7316efe023bfb9b61bec3414fd5b35a344e97114c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080915"
---
# <a name="shutting-down-a-multicast-routing-protocol"></a>Apagar un protocolo de enrutamiento de multidifusión

En la tabla siguiente se resume una serie de pasos en una interacción de apagado entre el administrador de grupos de multidifusión y el protocolo de enrutamiento cuando se cierra el protocolo de enrutamiento. En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del protocolo de enrutamiento al administrador de grupos de multidifusión. En la segunda columna se describen las respuestas del administrador de grupos de multidifusión al protocolo de enrutamiento y las acciones que realiza el administrador de grupos de multidifusión, como las devoluciones de llamada. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.



| Acción del protocolo de enrutamiento                                                                                                                                     | Acción del administrador de grupos de multidifusión                                                                                                                                                                                                                                                                                                                                                                                                                                            | Notas                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Libere la propiedad de cada interfaz que posee el protocolo de enrutamiento mediante la [**función MgmReleaseInterfaceOwnership.**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership) | Si IGMP también se ejecuta en la interfaz que acaba de publicar un protocolo de enrutamiento, póngase en contacto con IGMP mediante la devolución de llamada DE DEvolución de llamada [**\_ DE \_ IGMP \_ DISABLE DE PMGM.**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) Una vez realizados todos los cambios en los datos de multidifusión relacionados con la propiedad de la interfaz, vuelva a ponerse en contacto con IGMP con la devolución de llamada [**PMGM \_ ENABLE \_ IGMP \_ CALLBACK.**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)<br/> Elimine todas las entradas de reenvío asociadas a esta interfaz.<br/> |                                                                           |
| Anular el registro con el administrador de grupos de multidifusión [**mediante la función MgmDeRegisterMProtocol.**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)                                    | Destruye el identificador devuelto al protocolo de enrutamiento mediante una llamada anterior a la [**función MgmDeRegisterMProtocol.**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)                                                                                                                                                                                                                                                                                                                 | El protocolo de enrutamiento ya no puede usar este identificador para llamar a funciones MGM. |



 

 


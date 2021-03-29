---
title: Apagar un protocolo de enrutamiento de multidifusión
description: En la tabla siguiente se resume una serie de pasos en una interacción de apagado entre el administrador del grupo de multidifusión y el protocolo de enrutamiento cuando se está cerrando el protocolo de enrutamiento.
ms.assetid: d868218d-7939-45d1-9e2f-3415c40f1a62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d35285bdf613cb8ec5966fa438742004a97c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793144"
---
# <a name="shutting-down-a-multicast-routing-protocol"></a>Apagar un protocolo de enrutamiento de multidifusión

En la tabla siguiente se resume una serie de pasos en una interacción de apagado entre el administrador del grupo de multidifusión y el protocolo de enrutamiento cuando se está cerrando el protocolo de enrutamiento. En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del Protocolo de enrutamiento al administrador del grupo de multidifusión. En la segunda columna se describen las respuestas del administrador del grupo de multidifusión al Protocolo de enrutamiento y las acciones que realiza el administrador del grupo de multidifusión, como las devoluciones de llamada. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.



| Acción del Protocolo de enrutamiento                                                                                                                                     | Acción del administrador del grupo de multidifusión                                                                                                                                                                                                                                                                                                                                                                                                                                            | Notas                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Libera la propiedad de cada interfaz que el protocolo de enrutamiento posee mediante la función [**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership) . | Si IGMP también se está ejecutando en la interfaz que acaba de publicar mediante un protocolo de enrutamiento, póngase en contacto con IGMP mediante PMGM deshabilitar la devolución de llamada de [**\_ \_ \_ devoluciones de llamadas IGMP**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . Una vez que se hayan realizado todos los cambios en los datos de multidifusión relativos a la propiedad de la interfaz, póngase en contacto con IGMP de nuevo mediante PMGM habilitar la devolución de llamada [**\_ \_ IGMP \_**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback)<br/> Elimine todas las entradas de reenvío asociadas a esta interfaz.<br/> |                                                                           |
| Cancele el registro con el administrador del grupo de multidifusión mediante la función [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                    | Destruya el identificador que se devolvió al Protocolo de enrutamiento mediante una llamada anterior a la función [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                                                                                                                                                                                                                                                                                                 | El protocolo de enrutamiento ya no puede usar este identificador para llamar a las funciones MGM. |



 

 


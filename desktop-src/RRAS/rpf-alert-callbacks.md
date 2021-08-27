---
title: Devoluciones de llamada de alerta de RPF
description: Una vez que el administrador de grupos de multidifusión recibe la notificación de un paquete de un nuevo origen o de un paquete destinado a un nuevo grupo, el administrador de grupos de multidifusión busca la ruta al origen en la vista de multidifusión de la tabla de enrutamiento.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff1c2dc66b2307b60fb649fd8a0adb6992a63532bf9aa45350d261ab04b6c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035925"
---
# <a name="rpf-alert-callbacks"></a>Devoluciones de llamada de alerta de RPF

Una vez que el administrador de grupos de multidifusión recibe la notificación de un paquete de un nuevo origen o de un paquete destinado a un nuevo grupo, el administrador de grupos de multidifusión busca la ruta al origen en la vista de multidifusión de la tabla de enrutamiento. A continuación, el administrador de grupos de multidifusión invoca la devolución de llamada DE DEvolución de llamada [**\_ de RPF \_ pmgm**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) al protocolo que posee la interfaz en la que llegaron los datos.

Después de invocar esta devolución de llamada, el protocolo de enrutamiento puede cambiar la interfaz entrante si el protocolo de enrutamiento debe recibir los datos del grupo en una interfaz diferente.

 

 





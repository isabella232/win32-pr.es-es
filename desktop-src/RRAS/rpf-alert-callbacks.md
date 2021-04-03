---
title: Devoluciones de llamada de alerta de RPF
description: Una vez que el administrador del grupo de multidifusión recibe la notificación de un paquete de un nuevo origen o de un paquete destinado a un grupo nuevo, el administrador del grupo de multidifusión busca la ruta al origen en la vista multidifusión de la tabla de enrutamiento.
ms.assetid: dacccca2-e6a5-417a-a217-06ff846d55f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7832a25f8b44821f4b46a69943b4bba3519207c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780202"
---
# <a name="rpf-alert-callbacks"></a>Devoluciones de llamada de alerta de RPF

Una vez que el administrador del grupo de multidifusión recibe la notificación de un paquete de un nuevo origen o de un paquete destinado a un grupo nuevo, el administrador del grupo de multidifusión busca la ruta al origen en la vista multidifusión de la tabla de enrutamiento. Después, el administrador del grupo de multidifusión invoca la devolución de llamada de [**\_ devolución de \_ llamada de PMGM RPF**](/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback) al protocolo que posee la interfaz en la que llegaron los datos.

Después de invocar esta devolución de llamada, el protocolo de enrutamiento puede cambiar la interfaz entrante si el protocolo de enrutamiento debe recibir los datos para el grupo en una interfaz diferente.

 

 





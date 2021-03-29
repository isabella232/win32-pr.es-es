---
description: Los proveedores de servicios pueden exponer cada recurso de la PBX como un dispositivo de línea y, posiblemente, un dispositivo telefónico asociado.
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: Modelado de un centro de llamadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423607"
---
# <a name="modeling-of-a-call-center"></a>Modelado de un centro de llamadas

Los proveedores de servicios pueden exponer cada recurso de la PBX como un dispositivo de línea y, posiblemente, un dispositivo telefónico asociado. Los terminales que admiten varios aspectos de la llamada lo harían a través de varias direcciones, al igual que en el control de llamadas de primera parte. De hecho, la vista de otro fabricante de un dispositivo es idéntica a la vista de la primera parte; las aplicaciones del servidor pueden ver y controlar todos los dispositivos de la propia empresa, mientras que un equipo cliente individual conectado al servidor solo puede ver los dispositivos que están visibles en él a través de los controles de acceso administrados por TAPISRV en el servidor. Los recursos distintos de los terminales también pueden modelarse como dispositivos de línea. Por ejemplo, una cola o un punto de ruta de ACD se modelaría como un dispositivo de línea que podría tener muchas llamadas activas. también se podría modelar un servidor IVR, un servidor de correo de voz o un conjunto de puertos de marcado predictivo como un dispositivo de línea que admita varias llamadas.

Dentro de este modelo, el estado del dispositivo direccionado y las llamadas asociadas a él se pueden supervisar a través de mensajes TAPI existentes como la [**línea \_ LINEDEVSTATE**](line-linedevstate.md), la [**línea \_ ADDRESSSTATE**](line-addressstate.md), la [**línea \_ CALLSTATE**](line-callstate.md)y el [**\_ CALLINFO de línea**](line-callinfo.md)y los detalles obtenidos a través de funciones como [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus), [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus), [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)y [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo). Cada vez que se opera un objeto TAPI a través de una aplicación de otro fabricante que se ejecuta en el servidor, el resultado es idéntico al que se habría producido si el mismo objeto se hubiera utilizado de forma similar en una aplicación que se ejecuta en un equipo cliente asociado a ese dispositivo. Las indicaciones de estado enviadas por el proveedor de servicios de servidor que controlan el tejido de conmutación (o conmutador) se entregan tanto a las aplicaciones que se ejecutan en el servidor como a las que se ejecutan en clientes asociados y autorizados.

 

 




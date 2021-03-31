---
description: Describe el proceso de una operación de e/s de red en Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descripción de una operación de e/s de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371b72389554f1c3fa2ec43180b1a6e4c76dc012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360759"
---
# <a name="description-of-a-network-io-operation"></a>Descripción de una operación de e/s de red

En la ilustración siguiente se muestra el proceso de una operación de e/s de red en Windows.

![operación de e/s de red en Windows](images/fig4.png)

Cuando una aplicación llama a una función de e/s de archivo para tener acceso a un archivo en un equipo remoto, se producen los siguientes eventos:

-   La solicitud de e/s es interceptada por un [redirector de red](network-redirectors.md), también conocido como redirector, en el equipo local. Esto se muestra en la figura anterior mediante la flecha sólida entre la aplicación y el redirector del cliente.
-   El redirector crea un paquete de datos que contiene toda la información sobre la solicitud y lo envía al servidor donde se encuentra el archivo. Esto se muestra en la figura anterior mediante la flecha sólida entre el redirector del cliente y el redirector del servidor.
-   El redirector del servidor recibe el paquete del cliente, autentica el acceso al archivo requerido por la solicitud de e/s y, si se autentica, ejecuta la solicitud en nombre del cliente. En caso contrario, devuelve un código de error al Redirector en el cliente. Esto se muestra en la figura anterior por la flecha sólida curvada entre el redirector del servidor y el archivo.
-   Cuando se ha ejecutado la solicitud, el redirector en el servidor envía los datos resultantes de la solicitud de e/s al Redirector en el cliente junto con una notificación de operación correcta. Esto se muestra en la figura anterior por la flecha de puntos entre el servidor y el redirector del cliente.
-   El redirector del cliente recibe el paquete del servidor y pasa los datos del paquete a la aplicación junto con una notificación de éxito. Esto se muestra en la figura anterior por la flecha de puntos entre el redirector de cliente y la aplicación.

Windows puede usar una variedad de protocolos de red para realizar una operación de e/s de red, incluidos el [protocolo SMB de Microsoft y la información general sobre el protocolo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) y NFS.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Diferencias en la e/s local y de red](differences-in-local-and-network-i-o.md)<br/> | Diferencias entre la e/s local y la e/s de red en Windows.<br/> |
| [Redirectores de red](network-redirectors.md)<br/>                                   | Describe la funcionalidad de un redirector de red.<br/>      |



 

 

 





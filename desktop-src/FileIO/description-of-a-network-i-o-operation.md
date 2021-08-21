---
description: Describe el proceso de una operación de E/S de red en Windows.
ms.assetid: 72dc0c57-28ae-4289-bb0d-b399d294c126
title: Descripción de una operación de E/S de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d872f8eaf6f9a90ab313e6a7b17e3fe93073cdb13e5b039e401de41287f1c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150831"
---
# <a name="description-of-a-network-io-operation"></a>Descripción de una operación de E/S de red

En la ilustración siguiente se muestra el proceso de una operación de E/S de red en Windows.

![operación de E/S de red en Windows](images/fig4.png)

Cuando una aplicación llama a una función de E/S de archivo para acceder a un archivo en un equipo remoto, se producen los siguientes eventos:

-   La solicitud de E/S es interceptada por un [redirector](network-redirectors.md)de red, también denominado simplemente redirector, en el equipo local. Esto se muestra en la ilustración anterior mediante la flecha sólida entre la aplicación y el redirector de cliente.
-   El redirector crea un paquete de datos que contiene toda la información sobre la solicitud y lo envía al servidor donde se encuentra el archivo. Esto se muestra en la ilustración anterior mediante la flecha sólida entre el redirector de cliente y el redirector del servidor.
-   El redirector del servidor recibe el paquete del cliente, autentica el acceso al archivo requerido por la solicitud de E/S y, si se autentica, ejecuta la solicitud en nombre del cliente. Si no es así, devuelve un código de error al redirector en el cliente. Esto se muestra en la ilustración anterior mediante la flecha sólida curvada entre el redirector del servidor y el archivo.
-   Cuando se ha ejecutado la solicitud, el redirector del servidor envía los datos resultantes de la solicitud de E/S al redirector en el cliente junto con una notificación de éxito. Esto se muestra en la ilustración anterior mediante la flecha de puntos entre el servidor y el redirector de cliente.
-   El redirector del cliente recibe el paquete del servidor y pasa los datos del paquete a la aplicación junto con una notificación de éxito. Esto se muestra en la ilustración anterior mediante la flecha de puntos entre el redirector de cliente y la aplicación.

Windows usar una variedad de protocolos de red para realizar una operación de E/S de red, incluidos el protocolo SMB de Microsoft y la información general del protocolo [CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md) y NFS.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                          |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Diferencias en E/S local y de red](differences-in-local-and-network-i-o.md)<br/> | Diferencias entre E/S local y E/S de red en Windows.<br/> |
| [Redirectors de red](network-redirectors.md)<br/>                                   | Describe la funcionalidad de un redirector de red.<br/>      |



 

 

 





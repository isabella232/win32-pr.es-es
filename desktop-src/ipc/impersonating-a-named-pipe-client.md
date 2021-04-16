---
description: La suplantación es la capacidad de un subproceso de ejecutarse en un contexto de seguridad diferente del proceso que posee el subproceso.
ms.assetid: 1bde4d4d-958e-45f4-8cdb-0572adcaa3ac
title: Suplantar un cliente de canalización con nombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586de99ae24ba9bab8b65ba4cb1a3a91922aa9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686534"
---
# <a name="impersonating-a-named-pipe-client"></a>Suplantar un cliente de canalización con nombre

La *suplantación* es la capacidad de un subproceso de ejecutarse en un contexto de seguridad diferente del proceso que posee el subproceso. La suplantación permite que el subproceso de servidor realice acciones en nombre del cliente, pero dentro de los límites del contexto de seguridad del cliente. Normalmente, el cliente tiene algún menor nivel de derechos de acceso. Para obtener más información, vea [suplantación](/windows/desktop/SecAuthZ/client-impersonation).

Un subproceso de servidor de canalización con nombre puede llamar a la función [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) para asumir el token de acceso del usuario conectado al extremo de cliente de la canalización. Por ejemplo, un servidor de canalización con nombre puede proporcionar acceso a una base de datos o al sistema de archivos al que el servidor de canalización tiene privilegios de acceso. Cuando un cliente de canalización envía una solicitud al servidor, el servidor suplanta al cliente e intenta tener acceso a la base de datos protegida. A continuación, el sistema concede o deniega el acceso del servidor, en función del nivel de seguridad del cliente. Una vez finalizado el servidor, se usa la función [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para restaurar su token de seguridad original.

El [nivel de suplantación](/windows/desktop/SecAuthZ/impersonation-levels) determina las operaciones que el servidor puede realizar mientras suplanta al cliente. De forma predeterminada, un servidor suplanta el nivel de suplantación de SecurityImpersonation. Sin embargo, cuando el cliente llama a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador del extremo de cliente de la canalización, el cliente puede usar la \_ \_ marca SQOS de seguridad present para controlar el nivel de suplantación del servidor.

 

 

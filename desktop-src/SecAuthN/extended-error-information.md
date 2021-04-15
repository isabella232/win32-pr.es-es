---
description: Algunos paquetes de seguridad admiten mensajes de error extendidos que permiten a los lados de un vínculo de comunicación comunicar cualquier motivo de un error.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Información de error extendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648462"
---
# <a name="extended-error-information"></a>Información de error extendida

Algunos [*paquetes de seguridad*](/windows/desktop/SecGloss/s-gly) admiten mensajes de error extendidos que permiten a los lados de un vínculo de comunicación comunicar cualquier motivo de un error. Por ejemplo, el [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) podría producir un error debido a una discrepancia de tiempo entre el momento de la solicitud de un vale de Kerberos y la hora de emisión del vale. Con información de la información de error extendida, un cliente puede volver a sincronizar su reloj y generar un nuevo mensaje de conexión.

Un paquete de seguridad que establece \_ la \_ marca de error extendido de marca SECPKG \_ en el miembro **FCapabilities** de una estructura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) indica que el paquete de seguridad admite mensajes de error extendidos.

Las aplicaciones cliente que requieren mensajes de error extendidos especifican la \_ marca de error de solicitud \_ extendida de ISC \_ al llamar a la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Las aplicaciones de servidor que requieren mensajes de error extendidos establecen la \_ marca ASC req \_ Extended \_ error al llamar a [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).

 

 

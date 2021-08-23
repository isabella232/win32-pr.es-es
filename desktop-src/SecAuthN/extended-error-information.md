---
description: Algunos paquetes de seguridad admiten mensajes de error extendidos que permiten a los lados de un vínculo de comunicación comunicar cualquier motivo de un error.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Información de error extendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd93de1691a01802f65397abb1607612f5b7e61a311c9f801854a00c1ab4f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008223"
---
# <a name="extended-error-information"></a>Información de error extendida

Algunos [*paquetes de seguridad*](/windows/desktop/SecGloss/s-gly) admiten mensajes de error extendidos que permiten a los lados de un vínculo de comunicación comunicar cualquier motivo de un error. Por ejemplo, el [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) podría producir un error debido a una discrepancia de tiempo entre el momento de la solicitud de un vale de Kerberos y el momento del problema del vale. Con la información de la información de error extendida devuelta, un cliente puede resincronizar su reloj y generar un nuevo mensaje de conexión.

Un paquete de seguridad que establece la marca SECPKG FLAG EXTENDED ERROR en el miembro fCapabilities de una estructura SecPkgInfo indica que el paquete de seguridad admite mensajes \_ \_ de error \_ extendidos.  [](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)

Las aplicaciones cliente que requieren mensajes de error extendidos especifican la marca DE ERROR EXTENDIDO DE ISC REQ al llamar a la \_ \_ función \_ [**InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Las aplicaciones de servidor que requieren mensajes de error extendidos establecen la marca DE ERROR EXTENDIDO de ASC REQ al \_ \_ llamar a \_ [**AcceptSecurityContext (general).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

 

 

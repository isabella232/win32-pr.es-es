---
description: Algunos paquetes de seguridad admiten mensajes de error extendidos que permiten a los lados de un vínculo de comunicación comunicar cualquier motivo para un error.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Información de error extendida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271423"
---
# <a name="extended-error-information"></a>Información de error extendida

Algunos [*paquetes de seguridad*](/windows/desktop/SecGloss/s-gly) admiten mensajes de error extendidos que permiten a los lados de un vínculo de comunicación comunicar cualquier motivo para un error. Por ejemplo, el [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) podría producir un error debido a una discrepancia de tiempo entre el momento de la solicitud de un vale kerberos y la hora del problema del vale. Con la información de la información de error extendida devuelta, un cliente puede resincronizar su reloj y generar un nuevo mensaje de conexión.

Un paquete de seguridad que establece la marca SECPKG FLAG EXTENDED ERROR en el miembro fCapabilities de una \_ \_ estructura \_ [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)  indica que el paquete de seguridad admite mensajes de error extendidos.

Las aplicaciones cliente que requieren mensajes de error extendidos especifican la marca DE ERROR EXTENDIDO DE ISC REQ al llamar a \_ \_ la función \_ [**InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Las aplicaciones de servidor que requieren mensajes de error extendidos establecen la marca ASC \_ REQ \_ EXTENDED ERROR al llamar \_ a [**AcceptSecurityContext (general).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

 

 

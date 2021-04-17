---
description: El diseño de SSPI permite escribir y agregar SSP adicionales al sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Escribir e instalar un proveedor de soporte técnico de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667661"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Escribir e instalar un proveedor de soporte técnico de seguridad

El diseño de SSPI permite escribir y agregar SSP adicionales al sistema. Un [*SSP*](../secgloss/s-gly.md) específico de un modelo de seguridad se puede desarrollar con una complejidad relativa o extraordinaria, en función del nivel de integración con el sistema operativo. Un SSP de cliente que permite las conexiones a un nuevo tipo de servidor se puede desarrollar muy rápidamente, mientras que un SSP completo que proporciona suplantación local requiere más esfuerzo.

Los SSP se instalan mediante la actualización de un valor de **reg \_ SZ** en el registro, que se encuentra de la siguiente manera:

**HKEY \_ \_** \\ Control CurrentControlSet **del sistema** de equipo local \\  \\  \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            Registro \_ SZ</dd> </dl>

Un único archivo DLL puede contener varios SSP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones en relación con el registro y la instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 

---
description: El diseño de SSPI permite escribir y agregar más SSP al sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Escribir e instalar un proveedor de soporte técnico de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160866"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Escribir e instalar un proveedor de soporte técnico de seguridad

El diseño de SSPI permite escribir y agregar más SSP al sistema. Un [*SSP*](../secgloss/s-gly.md) específico de un modelo de seguridad se puede desarrollar con relativa facilidad o gran complejidad, en función del nivel de integración con el sistema operativo. Un SSP de cliente que permita conexiones a un nuevo tipo de servidor podría desarrollarse muy rápidamente, mientras que un SSP completo que proporciona la suplantación local requeriría más esfuerzo.

Los SSP se instalan mediante la actualización **de un valor REG \_ SZ** en el registro, ubicado de la siguiente manera:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            REG \_ SZ</dd> </dl>

Un solo archivo DLL puede contener varios SSP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Restricciones en torno al registro e instalación de un paquete de seguridad](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 

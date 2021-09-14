---
description: El modelo de seguridad usado en el protocolo SMB de Microsoft es idéntico al que usan otras variantes de SMB y consta de dos niveles de seguridad&\# 8212;usuario y recurso compartido.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticación de protocolo SMB de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069912"
---
# <a name="microsoft-smb-protocol-authentication"></a>Autenticación de protocolo SMB de Microsoft

El modelo de seguridad usado en el protocolo SMB de Microsoft es idéntico al que usan otras variantes de SMB y consta de dos niveles de seguridad: usuario y recurso compartido. Un recurso compartido es un archivo, directorio o impresora al que pueden acceder los clientes del Protocolo SMB de Microsoft.

La autenticación de nivel de usuario indica que el cliente que intenta acceder a un recurso compartido en un servidor debe proporcionar un nombre de usuario y una contraseña. Cuando se autentica, el usuario puede acceder a todos los recursos compartidos de un servidor que no está protegido por la seguridad de nivel de recurso compartido. Este nivel de seguridad permite a los administradores del sistema determinar específicamente qué usuarios y grupos pueden acceder a un recurso compartido.

La autenticación de nivel de recurso compartido indica que el acceso a un recurso compartido solo se controla mediante una contraseña asignada a ese recurso compartido. A diferencia de la seguridad de nivel de usuario, este nivel de seguridad no requiere un nombre de usuario para la autenticación y no se establece ninguna identidad de usuario.

En ambos niveles de seguridad, la contraseña se cifra antes de enviarse al servidor. [NTLM y](/windows/desktop/SecAuthN/microsoft-ntlm) el cifrado antiguo de LAN Manager (LM) son compatibles con el protocolo SMB de Microsoft. Ambos métodos de cifrado usan la autenticación desafío-respuesta, donde el servidor envía al cliente una cadena aleatoria y el cliente devuelve una cadena de respuesta calculada que demuestra que el cliente tiene credenciales suficientes para el acceso.

 

 

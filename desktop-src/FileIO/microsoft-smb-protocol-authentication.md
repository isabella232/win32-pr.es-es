---
description: El modelo de seguridad utilizado en el protocolo SMB de Microsoft es idéntico al utilizado por otras variantes de SMB y consta de dos niveles de seguridad&\# 8212; usuario y recurso compartido.
ms.assetid: 985aa9fe-af3f-406d-920d-7fd7d0d58674
title: Autenticación de protocolo SMB de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531e863b2a241bc861714980e6c5617e7d94e264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907901"
---
# <a name="microsoft-smb-protocol-authentication"></a>Autenticación de protocolo SMB de Microsoft

El modelo de seguridad utilizado en el protocolo SMB de Microsoft es idéntico al usado por otras variantes de SMB y consta de dos niveles de seguridad: usuario y recurso compartido. Un recurso compartido es un archivo, un directorio o una impresora a los que pueden tener acceso los clientes del protocolo SMB de Microsoft.

La autenticación de nivel de usuario indica que el cliente que intenta tener acceso a un recurso compartido en un servidor debe proporcionar un nombre de usuario y una contraseña. Cuando se autentica, el usuario puede tener acceso a todos los recursos compartidos de un servidor no protegido también por seguridad de nivel de recurso compartido. Este nivel de seguridad permite a los administradores del sistema determinar específicamente qué usuarios y grupos pueden tener acceso a un recurso compartido.

La autenticación de nivel de recurso compartido indica que el acceso a un recurso compartido solo está controlado por una contraseña asignada a ese recurso compartido. A diferencia de la seguridad de nivel de usuario, este nivel de seguridad no requiere un nombre de usuario para la autenticación y no se establece ninguna identidad de usuario.

En ambos niveles de seguridad, la contraseña se cifra antes de enviarla al servidor. [NTLM](/windows/desktop/SecAuthN/microsoft-ntlm) y el cifrado antiguo de LAN Manager (LM) son compatibles con el protocolo SMB de Microsoft. Ambos métodos de cifrado utilizan la autenticación de desafío-respuesta, donde el servidor envía al cliente una cadena aleatoria y el cliente devuelve una cadena de respuesta calculada que demuestra que el cliente tiene credenciales suficientes para el acceso.

 

 

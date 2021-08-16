---
description: Si esta directiva de sistema por máquina se establece en &\# 0034;1&0034;, el instalador escribe mensajes de depuración comunes en el depurador mediante la \# función OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3216b863953faa7edf3f8146084a0ec794f171482e0e619d717447ca0a0f30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692875"
---
# <a name="debug"></a>Depuración

Si esta directiva [](system-policy.md) de sistema por equipo se establece en "1", el instalador escribe mensajes de depuración comunes en el depurador mediante la [**función OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Si este valor se establece en "2", el instalador escribe todos los mensajes de depuración válidos en el depurador mediante la [**función OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Esta directiva solo tiene fines de depuración y es posible que no se puedan usar en versiones futuras de Windows Installer.

Windows El instalador solo escribe líneas de comandos en el archivo de registro si el tercer bit (0x04) se establece en el valor de la directiva de depuración. Por lo tanto, para mostrar las líneas de comandos en el registro, establezca el valor de la directiva de depuración en 7. Esto no muestra las propiedades asociadas a un [control de edición que](edit-control.md) tiene el atributo de control de [contraseña](password-control-attribute.md). Esto hará que las propiedades establecidas en la línea de comandos sean visibles en el registro, incluso si la propiedad está incluida en [**la propiedad MsiHiddenProperties.**](msihiddenproperties.md) Para obtener más información, vea [Impedir que la información confidencial se escriba en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 

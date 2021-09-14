---
description: Si esta directiva de sistema por equipo se establece en \# &0034;1&0034;, el instalador escribe mensajes de depuración comunes en el depurador mediante la \# función OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158620"
---
# <a name="debug"></a>Depurar

Si esta directiva del [sistema](system-policy.md) por máquina se establece en "1", el instalador escribe mensajes de depuración comunes en el depurador mediante la [**función OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Si este valor se establece en "2", el instalador escribe todos los mensajes de depuración válidos en el depurador mediante la [**función OutputDebugString.**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) Esta directiva solo tiene fines de depuración y es posible que no se puedan usar en versiones futuras de Windows Instalador.

Windows El instalador solo escribe líneas de comandos en el archivo de registro si el tercer bit (0x04) se establece en el valor de la directiva de depuración. Por lo tanto, para mostrar las líneas de comandos en el registro, establezca el valor de la directiva de depuración en 7. Esto no muestra las propiedades asociadas a un [control de edición que](edit-control.md) tiene el atributo de control de [contraseña](password-control-attribute.md). Esto hará que las propiedades establecidas en la línea de comandos sean visibles en el registro, incluso si la propiedad se incluye en [**la propiedad MsiHiddenProperties.**](msihiddenproperties.md) Para obtener más información, vea [Evitar que la información confidencial se escriba en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 

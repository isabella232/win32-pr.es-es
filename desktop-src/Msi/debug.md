---
description: Si esta Directiva del sistema por equipo está establecida en &\# 0034; 1&\# 0034;, el instalador escribe mensajes de depuración comunes en el depurador mediante la función OutputDebugString.
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: Depurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910981"
---
# <a name="debug"></a>Depurar

Si esta [Directiva del sistema](system-policy.md) por equipo se establece en "1", el instalador escribe mensajes de depuración comunes en el depurador mediante la función [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Si este valor se establece en "2", el instalador escribe todos los mensajes de depuración válidos en el depurador mediante la función [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) . Esta directiva solo se utiliza con fines de depuración y es posible que no se admita en versiones futuras de Windows Installer.

Windows Installer solo escribe las líneas de comandos en el archivo de registro si el tercer bit (0x04) se establece en el valor de la Directiva de depuración. Por lo tanto, para mostrar las líneas de comandos en el registro, establezca el valor de la Directiva de depuración en 7. Esto no muestra las propiedades asociadas a un [control de edición](edit-control.md) con el [atributo de control de contraseña](password-control-attribute.md). Esto hará que las propiedades establecidas en la línea de comandos sean visibles en el registro aunque la propiedad esté incluida en la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) . Para obtener más información, vea [impedir que se escriba información confidencial en el archivo de registro](preventing-confidential-information-from-being-written-into-the-log-file.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 

---
description: Si esta Directiva del sistema por equipo está establecida en &\# 0034; 1&\# 0034;, el instalador no solicitará a los usuarios que los scripts de una página web usen la interfaz de automatización del instalador.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666794"
---
# <a name="safeforscripting"></a>SafeForScripting

Si esta [Directiva del sistema](system-policy.md) por equipo se establece en "1", el instalador no solicitará a los usuarios cuando los scripts de una página web utilicen la [interfaz de automatización](automation-interface.md)del instalador.

Antes de establecer esta Directiva, debe considerar si, antes de la solicitud del usuario, se proporciona un nivel de seguridad adecuado para los usuarios. Si no se establece esta Directiva, cuando un script hospedado por un explorador de Internet intenta instalar una aplicación, el sistema advierte al usuario y le pide que acepte o rechace la instalación. La configuración de SafeForScripting suprime esta advertencia y puede permitir la instalación de aplicaciones en el sistema sin el conocimiento del usuario. Esta Directiva puede ser útil para una empresa que usa herramientas basadas en web para distribuir programas.

Para obtener más información, consulte [instrucciones para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md) y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md) y [descargar una instalación desde Internet](downloading-an-installation-from-the-internet.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 




---
description: Si esta directiva de sistema por máquina se establece en &\# 0034;1&0034;, el instalador no pregunta a los usuarios cuando los scripts de una página web usan la interfaz de automatización del \# instalador.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074306"
---
# <a name="safeforscripting"></a>SafeForScripting

Si esta directiva [](system-policy.md) de sistema por máquina se establece en "1", el instalador no pregunta a los usuarios cuando los scripts de una página web usan la interfaz de [automatización del instalador](automation-interface.md).

Antes de establecer esta directiva, debe considerar si la eliminación del aviso del usuario proporciona un nivel de seguridad adecuado para los usuarios. Si no se establece esta directiva, cuando un script hospedado por un explorador de Internet intenta instalar una aplicación, el sistema advierte al usuario y le pide que acepte o rechace la instalación. Al establecer SafeForScripting se suprime esta advertencia y se puede permitir la instalación de aplicaciones en el sistema sin que el usuario lo sepa. Esta directiva puede ser útil para una empresa que usa herramientas basadas en web para distribuir programas.

Para obtener más información, vea [Directrices](guidelines-for-authoring-secure-installations.md) para crear instalaciones seguras y [firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md) y Descargar una instalación de [Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 




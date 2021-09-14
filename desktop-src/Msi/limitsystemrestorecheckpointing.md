---
description: Esta directiva de sistema por equipo desactiva la creación de puntos de control Windows Instalador.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071968"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Esta directiva de sistema [por equipo](system-policy.md) desactiva la creación de puntos de control Windows Instalador.

Establecido en 0 o ausente, el instalador realiza puntos de control normales para la instalación o desinstalación. Establecido en 1, el instalador no crea ningún punto de control.

Esta directiva solo afecta a los puntos de control establecidos por Windows Instalador. En Windows XP, los administradores pueden decidir deshabilitar los puntos de control desde Windows Installer para mejorar el rendimiento. [**Restaurar sistema**](../sr/system-restore-portal.md) crea puntos de control adicionales. Para obtener más información, [vea Restaurar sistema y](system-restore-points-and-the-windows-installer.md) el instalador de Windows y Establecer un punto de [restauración a partir de una acción personalizada](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Clave del Registro

Establezca el valor denominado LimitSystemRestoreCheckpointing en la siguiente clave del Registro.

**HKEY \_ LOCAL MACHINE Software Policies Microsoft Windows \_ \\ \\ \\ \\ \\ Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 

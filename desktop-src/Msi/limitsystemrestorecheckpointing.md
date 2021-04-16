---
description: Esta Directiva del sistema por equipo desactiva la creación de puntos de control mediante Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686797"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Esta [Directiva del sistema](system-policy.md) por equipo desactiva la creación de puntos de control mediante Windows Installer.

Si se establece en 0 o ausente, el instalador realiza un punto de comprobación normal para la instalación o desinstalación. Si se establece en 1, el instalador no crea ningún punto de control.

Esta directiva solo afecta a los puntos de control establecidos por Windows Installer. En equipos con Windows XP, los administradores pueden decidir deshabilitar los puntos de comprobación desde Windows Installer para mejorar el rendimiento. [**Restaurar sistema**](../sr/system-restore-portal.md) también crea puntos de control adicionales. Para obtener más información, vea [puntos de restauración del sistema y el Windows Installer](system-restore-points-and-the-windows-installer.md) y [establecer un punto de restauración desde una acción personalizada](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Clave del Registro

Establezca el valor denominado LimitSystemRestoreCheckpointing en la siguiente clave del registro.

**HKEY \_ local \_ Machine \\ software \\ Policies \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 

---
description: Se trata de una directiva de sistema por equipo que se puede usar cuando el administrador solo quiere instalar aplicaciones por máquina.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158534"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Se trata de una directiva de [sistema por](system-policy.md) equipo que se puede usar cuando el administrador solo quiere instalar aplicaciones por máquina.

Si no se establece esta directiva, el instalador busca aplicaciones en el Registro en el orden siguiente: aplicaciones administradas registradas como por usuario, aplicaciones no administradas registradas como por usuario y, por último, aplicaciones registradas como por equipo.

Si esta directiva se establece en 1, el instalador omite todas las aplicaciones registradas como por usuario y solo busca aplicaciones registradas como por equipo. Las llamadas a la interfaz de programación de Windows Installer o al sistema omiten las aplicaciones por usuario. Un intento de realizar una instalación [](installation-context.md) en el contexto de instalación por usuario hace que el instalador muestre un mensaje de error y detenga la instalación. En este caso, el instalador Windows también impide las instalaciones por usuario desde un servidor terminal.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 




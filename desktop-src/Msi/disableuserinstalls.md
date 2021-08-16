---
description: Se trata de una directiva de sistema por máquina que se puede usar cuando el administrador solo quiere instalar aplicaciones por máquina.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 171c003dbe739c890bf15e5c372e40840fee0aabc9159a837c0b5572a8741b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378518"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Se trata de una directiva de [sistema por](system-policy.md) máquina que se puede usar cuando el administrador solo quiere instalar aplicaciones por máquina.

Si no se establece esta directiva, el instalador busca aplicaciones en el registro en el orden siguiente: aplicaciones administradas registradas como por usuario, aplicaciones no administradas registradas como por usuario y, por último, aplicaciones registradas como por equipo.

Si esta directiva se establece en 1, el instalador omite todas las aplicaciones registradas como por usuario y solo busca aplicaciones registradas como por equipo. Las llamadas a la interfaz de programación de aplicaciones Windows Installer o al sistema omiten las aplicaciones por usuario. Un intento de realizar una instalación [](installation-context.md) en el contexto de instalación por usuario hace que el instalador muestre un mensaje de error y detenga la instalación. En este caso, el instalador de Windows también impide las instalaciones por usuario desde un servidor de Terminal Server.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 




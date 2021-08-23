---
description: HKLM \\ Software Microsoft Internet Explorer \\ \\ \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93228857af2e531360b6238ab649daf8ac3f9eb2acf0aecfb12348b0ed990b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795245"
---
# <a name="exec"></a>Exec

**HKLM \\ Software Microsoft Internet Explorer \\ \\ \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Tipo de datos | Intervalo                    | Valor predeterminado |
|-----------|--------------------------|---------------|
| REG \_ SZ   | *Ruta de acceso al ejecutable* |               |



 

## <a name="browser-integration-steps"></a>Pasos de integración del explorador

1.  Use la [**función RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para determinar si el diagnóstico de red está instalado. Si está instalado, la clave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** está presente.
2.  Use la [**función RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para recuperar la ruta de acceso del archivo ejecutable de diagnóstico de red de la **entrada Exec.**
3.  Muestra la nueva página de error si el diagnóstico está instalado en el sistema.
4.  Cree una extensión del explorador que cree un elemento de la barra de herramientas estándar si el diagnóstico está instalado en el sistema.
5.  Ejecute el ejecutable De diagnóstico de red mediante la ruta de acceso recuperada en el paso 2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre las características de las herramientas de diagnóstico de red](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 

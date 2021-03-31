---
description: HKLM \\ software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807718"
---
# <a name="exec"></a>Exec

**HKLM \\ software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**



| Tipo de datos | Intervalo                    | Valor predeterminado |
|-----------|--------------------------|---------------|
| Registro \_ SZ   | *Ruta de acceso al archivo ejecutable* |               |



 

## <a name="browser-integration-steps"></a>Pasos de integración del explorador

1.  Use la función [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) para determinar si el diagnóstico de red está instalado. Si está instalado, la clave **{e2e2dd38-d088-4134-82b7-f2ba38496583}** está presente.
2.  Use la función [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para recuperar la ruta de acceso del archivo ejecutable de diagnóstico de red de la entrada **exec** .
3.  Muestra la nueva página de error si el diagnóstico está instalado en el sistema.
4.  Cree una extensión de explorador que cree un elemento de la barra de herramientas estándar si el diagnóstico está instalado en el sistema.
5.  Ejecute el archivo ejecutable de diagnóstico de red mediante la ruta de acceso recuperada en el paso 2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre las características de diagnóstico de red](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 

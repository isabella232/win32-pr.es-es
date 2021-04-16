---
title: Pruebas con AccChecker
description: Describe el flujo de trabajo de pruebas típico que incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- pruebas con AccChecker
- AccChecker, flujo de trabajo de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531906"
---
# <a name="testing-with-accchecker"></a>Pruebas con AccChecker

En el escenario siguiente se describen los pasos que suele seguir al realizar pruebas con AccChecker.

> [!Note]  
> Cuando se ejecutan rutinas de comprobación de AccChecker, la interacción del usuario con el equipo host puede interferir con algunas rutinas. Se recomienda que no se produzca ninguna interacción del usuario hasta que AccChecker notifique al usuario que se han completado todas las tareas.

 

1.  Ejecute comprobaciones de AccChecker en una aplicación o un control de destino determinados. Para obtener más información, consulte la [pestaña comprobaciones](the-accchecker-graphical-user-interface.md).
    > [!Note]  
    > AccChecker no explora todas las permutaciones de la interfaz de usuario de una aplicación. Los elementos ocultos en controles como ventanas, paneles, pestañas y menús deben exponerse manualmente.

     

2.  Examine el registro de errores de AccChecker y evalúe o clasifique los resultados. Corrija los problemas triviales y registre los errores graves según corresponda.
3.  Generar un archivo de supresión para errores y errores que se pueden omitir hasta las pruebas de regresión.
4.  Vuelva a ejecutar las comprobaciones de AccChecker con el archivo de supresión y las correcciones de errores iniciales. Esto proporciona una instantánea de los problemas en la implementación actual de Microsoft Active Accessibility y establece una línea base para las pruebas de regresión.
5.  Integre las API de AccChecker y el archivo de supresión en un marco de pruebas automatizadas para las pruebas de regresión en los errores registrados en las comprobaciones de AccChecker iniciales.
    > [!Note]  
    > A medida que se corrijan los errores, el archivo de supresión debe modificarse según sea necesario.

     

6.  Confirme que no se han introducido regresiones ni nuevos errores de accesibilidad en la aplicación o el control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





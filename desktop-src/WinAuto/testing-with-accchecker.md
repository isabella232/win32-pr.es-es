---
title: Pruebas con AccChecker
description: Describe el flujo de trabajo de pruebas típico que incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- pruebas con AccChecker
- AccChecker, flujo de trabajo de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addf725431a17a9b63376dfc3fc7ef8563a1737c9867b950f09eb123bf7daf18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795515"
---
# <a name="testing-with-accchecker"></a>Pruebas con AccChecker

En el escenario siguiente se describen los pasos que normalmente se siguen al realizar pruebas con AccChecker.

> [!Note]  
> Cuando se ejecutan rutinas de comprobación de AccChecker, la interacción del usuario con el equipo host puede interferir con algunas rutinas. Se recomienda que no se produzca ninguna otra interacción del usuario hasta que AccChecker notime al usuario que se han completado todas las tareas.

 

1.  Ejecute las comprobaciones de AccChecker en una aplicación o control de destino determinado. Para obtener más información, vea [La pestaña Comprobaciones](the-accchecker-graphical-user-interface.md).
    > [!Note]  
    > AccChecker no explora todas las permutaciones de interfaz de usuario en una aplicación. Los elementos ocultos dentro de controles como ventanas, paneles, pestañas y menús deben exponerse manualmente.

     

2.  Examine el registro de errores de AccChecker y evalúe o evalue los resultados. Corrija problemas triviales y registre errores graves según corresponda.
3.  Genere un archivo de supresión para errores y errores que se pueden omitir hasta las pruebas de regresión.
4.  Vuelva a ejecutar las comprobaciones de AccChecker con el archivo de supresión y las correcciones de errores iniciales. Esto proporciona una instantánea de los problemas de la implementación actual de Microsoft Active Accessibility establece una línea base para las pruebas de regresión.
5.  Integre las API de AccChecker y el archivo de supresión en un marco de pruebas automatizado para las pruebas de regresión en los errores registrados desde las comprobaciones iniciales de AccChecker.
    > [!Note]  
    > A medida que se corrigirán los errores, el archivo de supresión debe modificarse según sea necesario.

     

6.  Confirme que no se han introducido regresiones ni nuevos errores de accesibilidad en la aplicación o el control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





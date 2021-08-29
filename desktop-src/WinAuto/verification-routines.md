---
title: Rutinas de comprobación
description: En esta sección se describen las rutinas de comprobación que el comprobador de accesibilidad de la interfaz de usuario puede ejecutar para probar la implementación de accesibilidad de una aplicación.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352a56b15a376af3d378def6fd49f04775063f4928fb87444107f7671c9d51ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997665"
---
# <a name="verification-routines"></a>Rutinas de comprobación

En esta sección se describen las rutinas de comprobación que el comprobador de accesibilidad de la interfaz de usuario puede ejecutar para probar la implementación de accesibilidad de una aplicación.



<table>
<thead>
<tr class="header">
<th>Category</th>
<th>Rutina</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Coherencia</strong>${REMOVE}$<br />
</td>
<td><strong>ScreenReader</strong></td>
<td>Compila todos los elementos visibles en el destino de comprobación y los muestra en un control ListView en el orden en que un lector de pantalla estándar los anuncia a un usuario.</td>
</tr>
<tr class="even">
<td><strong>UiaScreenReader</strong></td>
<td>Igual que <strong>ScreenReader,</strong>pero para implementaciones de UIA.</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>Navegación</strong>${REMOVE}$<br />
</td>
<td><strong>CheckTreeDepth</strong></td>
<td>Envía caracteres tab (o Mayús+Tab) como entrada al destino de comprobación para confirmar que la interfaz de usuario del destino no es demasiado compleja o inaccesible mediante la navegación con el teclado estándar.</td>
</tr>
<tr class="even">
<td><strong>CheckTabbingUia</strong></td>
<td>Envía caracteres tab (o Mayús+Tab) como entrada al destino de comprobación para confirmar que todos los elementos que se pueden centrar en la interfaz de usuario son accesibles de forma ordenada y lógica mediante la navegación con el teclado estándar.</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Propiedades</strong>${REMOVE}$<br />
</td>
<td><strong>CheckRole</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un rol MSAA lógico válido y que el control tiene un valor según sea necesario para ese rol.</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un estado MSAA lógico válido.</td>

</tr>
<tr class="odd">
<td><strong>CheckName</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un nombre MSAA lógico válido.</td>

</tr>
<tr class="even">
<td><strong>CheckAccessKeys</strong></td>
<td>Confirma que las claves de acceso asignadas a los elementos del destino de comprobación son únicas dentro del destino de comprobación.</td>

</tr>
<tr class="odd">
<td><strong>CheckBoundingRect</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario tiene un rectángulo delimitador que se puede usar como destino para las pruebas de impacto.</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Árbol</strong>${REMOVE}$<br />
</td>
<td><strong>CheckParentChild</strong></td>
<td>Las relaciones primarias y secundarias del árbol de elementos son coherentes y predecibles.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildren</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un elemento primario MSAA válido.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Propiedades de UIA</strong>${REMOVE}$<br />
</td>
<td><strong>CheckNameUIA</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un nombre UIA lógico válido.</td>
</tr>
<tr class="odd">
<td><strong>CheckTreeDepthUIA</strong></td>
<td>Envía caracteres tab (o Mayús+Tab) como entrada al destino de comprobación para confirmar que los elementos UIA de la interfaz de usuario del destino no son demasiado complejos o inaccesibles mediante la navegación con el teclado estándar.</td>

</tr>
<tr class="even">
<td><strong>CheckStateUIA</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un estado UIA lógico válido.</td>

</tr>
<tr class="odd">
<td><strong>CheckAccessKeysUIA</strong></td>
<td>Confirma que los elementos del mismo nivel no tienen el mismo acceso o tecla de aceleración.</td>

</tr>
<tr class="even">
<td><strong>CheckBoundingRectUIA</strong></td>
<td>Confirma que cada elemento UIA que se puede centrar en la interfaz de usuario tiene un rectángulo delimitador que se puede usar como destino para las pruebas de impacto.</td>

</tr>
<tr class="odd">
<td><strong>CheckControlTypeUIA</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un tipo de control UIA lógico válido.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Árbol UIA</strong>${REMOVE}$<br />
</td>
<td><strong>CheckNavigateUia</strong></td>
<td>Confirma que UIA TreeWalker puede navegar por los elementos secundarios de un elemento.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildrenUia</strong></td>
<td>Confirma que cada elemento que se puede centrar en la interfaz de usuario notifica un elemento primario UIA válido.</td>

</tr>
<tr class="even">
<td><strong>CheckSiblingsUia</strong></td>
<td>Confirma que los elementos del mismo nivel no tienen los mismos pares Name:ControlType ni los mismos AutomationId.</td>

</tr>
<tr class="odd">
<td>${ROWSPAN9}$<strong>Comprobaciones web</strong>de ARIA ${REMOVE}$<br />
</td>
<td><strong>CheckARIARole</strong></td>
<td>Confirma que todos los elementos tienen un rol ARIA válido. La etiqueta HTML asociada y el rol ARIA son elementos de información con roles no válidos marcados como errores.</td>
</tr>
<tr class="even">
<td><strong>CheckLabel</strong></td>
<td>Confirma que cada elemento con entrada, botón, botón de imagen o rol de punto de referencia tiene una etiqueta.</td>

</tr>
<tr class="odd">
<td><strong>CheckRangeControls</strong></td>
<td>Confirma que los controles de intervalo con el control deslizante o el rol de barra de progreso tienen definidos los atributos ARIA adecuados.</td>

</tr>
<tr class="even">
<td><strong>CheckContainerRole</strong></td>
<td>Confirma que un elemento, o al menos uno de sus elementos secundarios, tiene definido onkeydown/onkeypress.</td>

</tr>
<tr class="odd">
<td><strong>CheckLayoutTable</strong></td>
<td>Confirma que un diseño de tabla tiene un resumen/th/aria-describedby incluido.</td>

</tr>
<tr class="even">
<td><strong>CheckGridStructure</strong></td>
<td>Confirma que un elemento que no es de tabla con el rol de cuadrícula tiene una estructura de cuadrícula>fila>celda de cuadrícula con atributos asociados.</td>

</tr>
<tr class="odd">
<td><strong>CheckDataTable</strong></td>
<td>Confirma las propiedades de las tablas de datos.</td>

</tr>
<tr class="even">
<td><strong>CheckActiveDescendants</strong></td>
<td>Confirma las propiedades de los elementos con un descendiente activo definido.</td>

</tr>
<tr class="odd">
<td><strong>CheckElementsWithClickHandler</strong></td>
<td>Confirma el índice de tabulación de los elementos con controladores de clic.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Comprobaciones web</strong>${REMOVE}$<br />
</td>
<td><strong>CheckHtml (Web)</strong></td>
<td>Confirma varias características HTML, como encabezados, nombres, marcos y títulos.</td>
</tr>
<tr class="odd">
<td><strong>CheckName (Web)</strong></td>
<td>Confirma las características del nombre, como la longitud, los caracteres no válidos y la inclusión de roles.</td>

</tr>
<tr class="even">
<td><strong>CheckRole (Web)</strong></td>
<td>Confirma roles no válidos, roles que deben tener valores o roles no implementados.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





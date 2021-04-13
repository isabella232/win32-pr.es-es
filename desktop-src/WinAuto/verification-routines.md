---
title: Rutinas de comprobación
description: En esta sección se describen las rutinas de comprobación que puede ejecutar el comprobador de accesibilidad de la interfaz de usuario para probar la implementación de accesibilidad de una aplicación.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357157"
---
# <a name="verification-routines"></a>Rutinas de comprobación

En esta sección se describen las rutinas de comprobación que puede ejecutar el comprobador de accesibilidad de la interfaz de usuario para probar la implementación de accesibilidad de una aplicación.



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
<td rowspan="2"><strong>Coherencia</strong>$ {Remove} $<br />
</td>
<td><strong>ScreenReader</strong></td>
<td>Compila todos los elementos visibles en el destino de comprobación y los muestra en un control ListView en el orden en que un lector de pantalla estándar los anuncia a un usuario.</td>
</tr>
<tr class="even">
<td><strong>UiaScreenReader</strong></td>
<td>Igual que <strong>ScreenReader</strong>, pero para implementaciones de UIA.</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>Navegación</strong>$ {Remove} $<br />
</td>
<td><strong>CheckTreeDepth</strong></td>
<td>Envía caracteres de tabulación (o Mayús + Tab) como entrada al destino de comprobación para confirmar que la interfaz de usuario del destino no es demasiado compleja o inaccesible mediante la navegación de teclado estándar.</td>
</tr>
<tr class="even">
<td><strong>CheckTabbingUia</strong></td>
<td>Envía caracteres de tabulación (o Mayús + Tab) como entrada al destino de comprobación para confirmar que todos los elementos que pueden recibir el foco en la interfaz de usuario son accesibles de forma ordenada y lógica mediante la navegación de teclado estándar.</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Propiedades</strong>$ {Remove} $<br />
</td>
<td><strong>CheckRole</strong></td>
<td>Confirma que cada elemento que tiene el foco en la interfaz de usuario notifica un rol de MSAA lógico y válido, y que el control tiene un valor según sea necesario para ese rol.</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un estado de MSAA lógico y válido.</td>

</tr>
<tr class="odd">
<td><strong>CheckName</strong></td>
<td>Confirma que cada elemento enfocable de la interfaz de usuario informa de un nombre de MSAA lógico y válido.</td>

</tr>
<tr class="even">
<td><strong>CheckAccessKeys</strong></td>
<td>Confirma que las claves de acceso que se asignan a los elementos del destino de comprobación son únicas en el destino de la comprobación.</td>

</tr>
<tr class="odd">
<td><strong>CheckBoundingRect</strong></td>
<td>Confirma que cada elemento enfocable de la interfaz de usuario tiene un rectángulo delimitador que se puede usar como destino para la prueba de posicionamiento.</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Árbol</strong>$ {Remove} $<br />
</td>
<td><strong>CheckParentChild</strong></td>
<td>Las relaciones primarias y secundarias en el árbol de elementos son coherentes y predecibles.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildren</strong></td>
<td>Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un elemento primario de MSAA válido.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Propiedades de UIA</strong>$ {Remove} $<br />
</td>
<td><strong>CheckNameUIA</strong></td>
<td>Confirma que cada elemento enfocable de la interfaz de usuario informa de un nombre válido de UIA lógico.</td>
</tr>
<tr class="odd">
<td><strong>CheckTreeDepthUIA</strong></td>
<td>Envía caracteres de tabulación (o Mayús + Tab) como entrada al destino de comprobación para confirmar que los elementos de UIA en la interfaz de usuario de destino no son demasiado complejos o inaccesibles mediante la navegación de teclado estándar.</td>

</tr>
<tr class="even">
<td><strong>CheckStateUIA</strong></td>
<td>Confirma que cada elemento enfocable de la interfaz de usuario informa de un estado válido y lógico de UIA.</td>

</tr>
<tr class="odd">
<td><strong>CheckAccessKeysUIA</strong></td>
<td>Confirma que los elementos relacionados no tienen el mismo acceso o la misma tecla de aceleración.</td>

</tr>
<tr class="even">
<td><strong>CheckBoundingRectUIA</strong></td>
<td>Confirma que cada elemento de UIA enfocable en la interfaz de usuario tiene un rectángulo delimitador que se puede usar como destino para la prueba de posicionamiento.</td>

</tr>
<tr class="odd">
<td><strong>CheckControlTypeUIA</strong></td>
<td>Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un tipo de control de UIA lógico y válido.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Árbol de UIA</strong>$ {Remove} $<br />
</td>
<td><strong>CheckNavigateUia</strong></td>
<td>Confirma que el TreeWalker de UIA puede navegar por los elementos secundarios de un elemento.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildrenUia</strong></td>
<td>Confirma que cada elemento que tiene el foco en la interfaz de usuario informa de un elemento primario de UIA válido.</td>

</tr>
<tr class="even">
<td><strong>CheckSiblingsUia</strong></td>
<td>Confirma que los elementos del mismo nivel no tienen el mismo nombre: pares ControlType, ni el mismo elemento AutomationId.</td>

</tr>
<tr class="odd">
<td>$ {ROWSPAN9} $<strong>Aria web verificaciones</strong>$ {Remove} $<br />
</td>
<td><strong>CheckARIARole</strong></td>
<td>Confirma que todos los elementos tienen un rol de ARIA válido. La etiqueta HTML y el rol ARIA asociados son elementos de información con roles no válidos marcados como errores.</td>
</tr>
<tr class="even">
<td><strong>CheckLabel</strong></td>
<td>Confirma que cada elemento con la entrada, el botón, el botón de imagen o el rol de punto de referencia tiene una etiqueta.</td>

</tr>
<tr class="odd">
<td><strong>CheckRangeControls</strong></td>
<td>Confirma que los controles de intervalo con el control deslizante o el rol de barra de progreso tienen definidos los atributos ARIA adecuados.</td>

</tr>
<tr class="even">
<td><strong>CheckContainerRole</strong></td>
<td>Confirma un elemento, o al menos uno de sus elementos secundarios, y ha definido onkeydown/onkeypress.</td>

</tr>
<tr class="odd">
<td><strong>CheckLayoutTable</strong></td>
<td>Confirma que un diseño de tabla tiene una Summary/TH/Aria-describedby incluida.</td>

</tr>
<tr class="even">
<td><strong>CheckGridStructure</strong></td>
<td>Confirma que un elemento que no es de tabla con el rol de cuadrícula tiene una estructura de cuadrícula>fila>gridcell con atributos asociados.</td>

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
<td rowspan="3"><strong>Comprobaciones web</strong>$ {Remove} $<br />
</td>
<td><strong>CheckHtml (Web)</strong></td>
<td>Confirma varias características HTML como encabezados, nombre, marcos y títulos.</td>
</tr>
<tr class="odd">
<td><strong>CheckName (Web)</strong></td>
<td>Confirma características de nombre como la longitud, los caracteres no válidos y la inclusión de roles.</td>

</tr>
<tr class="even">
<td><strong>CheckRole (Web)</strong></td>
<td>Confirma roles no válidos, roles que deben tener valores y/o roles no implementados.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





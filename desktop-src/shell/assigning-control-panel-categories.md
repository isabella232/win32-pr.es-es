---
description: A partir de Windows XP, el panel de control admite la categorización de elementos del panel de control. Los elementos se registran para aparecer en una o varias categorías. No se pueden crear nuevas categorías.
title: Asignar categorías del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: bade62cda23c2d2f66ffdfd70f3f555a243f3efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984363"
---
# <a name="assigning-control-panel-categories"></a>Asignar categorías del panel de control

A partir de Windows XP, el panel de control admite la categorización de elementos del panel de control. Los elementos se registran para aparecer en una o varias categorías. No se pueden crear nuevas categorías.

Para registrar un elemento del panel de control en una o varias categorías, agregue valores como se explica en la sección registro de elementos del panel de [control ejecutable](registering-control-panel-items.md) o registro de elementos del panel de control de [dll](registering-control-panel-items.md) de registro de [elementos del panel](registering-control-panel-items.md)de control, según corresponda.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Id. de categoría</th>
<th>Nombre de categoría (Windows 7)</th>
<th>Nombre de categoría (Windows Vista)</th>
<th>Nombre de categoría (Windows XP)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>&quot;Todos los elementos del panel de control&quot;</td>
<td>&quot;Opciones adicionales&quot;
<blockquote>
[!Note]<br />
En esta categoría aparece cualquier elemento del panel de control que no especifique un ID. de categoría.
</blockquote>
<br/></td>
<td>&quot;Otras opciones del panel de control&quot;
<blockquote>
[!Note]<br />
En esta categoría aparece cualquier elemento del panel de control que no especifique un ID. de categoría.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>1</td>
<td>&quot;Apariencia y personalización&quot;</td>
<td>&quot;Apariencia y personalización&quot;</td>
<td>&quot;Apariencia y temas&quot;</td>
</tr>
<tr class="odd">
<td>2</td>
<td>&quot;Hardware y sonido&quot;</td>
<td>&quot;Hardware y sonido&quot;</td>
<td>&quot;Impresoras y otro hardware&quot;</td>
</tr>
<tr class="even">
<td>3</td>
<td>&quot;Red e Internet&quot;</td>
<td>&quot;Red e Internet&quot;</td>
<td>&quot;Conexiones de red e Internet&quot;</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Ya no se usa. Los elementos que se agregan solo a la categoría 4 aparecen en categoría 2 (hardware y sonido).</td>
<td>Ya no se usa. Los elementos que se agregan solo a la categoría 4 aparecen en categoría 2 (hardware y sonido).</td>
<td>&quot;Dispositivos de sonido, voz y audio&quot;</td>
</tr>
<tr class="even">
<td>5</td>
<td>&quot;Sistema y seguridad&quot;</td>
<td>&quot;Sistema y mantenimiento&quot;</td>
<td>&quot;Rendimiento y mantenimiento&quot;</td>
</tr>
<tr class="odd">
<td>6</td>
<td>&quot;Reloj, idioma y región&quot;</td>
<td>&quot;Reloj, idioma y región&quot;</td>
<td>&quot;Opciones de fecha, hora, idioma y configuración regional&quot;</td>
</tr>
<tr class="even">
<td>7</td>
<td>&quot;Facilidad de acceso&quot;</td>
<td>&quot;Facilidad de acceso&quot;</td>
<td>&quot;Opciones de accesibilidad&quot;</td>
</tr>
<tr class="odd">
<td>8</td>
<td>&quot;Programs&quot;</td>
<td>&quot;Programs&quot;</td>
<td>&quot;Agregar o quitar programas&quot;</td>
</tr>
<tr class="even">
<td>9</td>
<td>&quot;Cuentas de usuario&quot;
<blockquote>
[!Note]<br />
Cuando no está conectado a un dominio, esto se denomina &quot; cuentas de usuario y seguridad de la familia &quot; .
</blockquote>
<br/></td>
<td>&quot;Cuentas de usuario&quot;
<blockquote>
[!Note]<br />
Cuando no está conectado a un dominio, esto se denomina &quot; cuentas de usuario y seguridad de la familia &quot; .
</blockquote>
<br/></td>
<td>&quot;Cuentas de usuario&quot;</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Ya no se usa. Los elementos registrados en esta categoría aparecen en categoría 5 (sistema y seguridad).</td>
<td>&quot;Seguridad&quot;</td>
<td>&quot;Centro de seguridad&quot;
<blockquote>
[!Note]<br />
Solo disponible en Windows XP Service Pack 2 (SP2) o posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>11</td>
<td>Ya no se usa. Los elementos registrados en esta categoría aparecen en la categoría 0 (todos los elementos del panel de control).</td>
<td>&quot;PC móvil&quot;
<blockquote>
[!Note]<br />
Esta categoría solo está visible en PC móviles.
</blockquote>
<br/></td>
<td>No se utiliza.</td>
</tr>
</tbody>
</table>



 

En Windows XP, las categorías **Agregar o quitar programas** y **cuentas de usuario** funcionan de forma ligeramente diferente a otras categorías del panel de control. Cuando se agregan uno o varios elementos a una de estas dos categorías, el vínculo asociado del panel de control abre una página de categorías. Los elementos registrados aparecen en la parte inferior de la página bajo el encabezado "o seleccionar un icono del panel de control". Cuando no se registra ningún elemento para una de estas categorías, el vínculo asociado del panel de control invoca directamente el elemento estándar de Windows para esa categoría. En Windows Vista y versiones posteriores, la categoría **programas** y la categoría **cuentas de usuario** no tienen esta propiedad.

La categoría **Security Center** , disponible únicamente en Windows XP SP2, también es algo no estándar. Al hacer clic en esta categoría, se abre la página **Security Center** en una nueva ventana. Los elementos registrados para **Security Center** aparecen en la parte inferior de la página en el encabezado **administrar la configuración de seguridad de:**. Al hacer clic en un icono, se abre el elemento del panel de control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Usar CPLApplet](using-cplapplet.md)
</dt> <dt>

[Procesamiento de mensajes del panel de control](message-processing.md)
</dt> <dt>

[Ejecutar elementos del panel de control](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos del panel de control del sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md)
</dt> <dt>

[Acceder al panel de control en modo seguro en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 





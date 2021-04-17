---
description: La tabla PatchMetadata contiene información acerca de una revisión Windows Installer necesaria para quitar una revisión y que se usa en Agregar o quitar programas.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabla PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653053"
---
# <a name="patchmetadata-table-patchwizdll"></a>Tabla PatchMetadata (PATCHWIZ.DLL)

La tabla PatchMetadata contiene información acerca de una revisión Windows Installer necesaria para quitar una revisión y que se usa en Agregar o quitar programas. Todas las propiedades de la tabla PatchMetadata se agregan a la [tabla MsiPatchMetadata](msipatchmetadata-table.md) del archivo. msp para una revisión.

La tabla PatchMetadata es necesaria en los archivos de propiedades de creación de revisiones (archivos. PCP) que tienen un valor de MinimumRequiredMsiVersion igual a 300 en la [tabla de propiedades](properties-table-patchwiz-dll-.md). La tabla es opcional si MinimumRequiredMsiVersion no es igual a 300.

La tabla PatchMetadata tiene las columnas siguientes.



| Columna   | Tipo | Clave | Nullable |
|----------|------|-----|----------|
| Compañía  | text | Y   | Y        |
| Propiedad | text | Y   | N        |
| Value    | text |     | Y        |



 

### <a name="columns"></a>Columnas

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Recíproca
</dt> <dd>

El nombre de la empresa. Un campo vacío (un valor null) indica que esta fila contiene una de las propiedades de metadatos estándar. Una empresa puede extender el conjunto de propiedades agregando una fila a la tabla y especificando un nombre de compañía en este campo.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Nombre de una propiedad de metadatos. Las propiedades AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description y Classification son necesarias en la tabla PatchMetadata. Este campo debe contener una de las siguientes propiedades de metadatos estándar si el campo Company está vacío (un valor null).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowRemoval</td>
<td>Un valor entero que indica si la revisión es o no una <a href="uninstallable-patches.md">revisión desinstalable</a>. Si el campo de valor contiene un 0 (cero), no se puede quitar la revisión. Si el campo de valor contiene 1 (uno), la revisión es una revisión que no se pudo instalar. Esta propiedad es obligatoria. Esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>Valor de cadena que contiene el nombre del fabricante de la aplicación. Esta propiedad es obligatoria.</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>Indica que la revisión tiene como destino la versión RTM del producto o la revisión de actualización principal más reciente. Cree esta propiedad opcional en revisiones de actualización secundarias que contengan información de secuenciación para indicar que la revisión quita todas las revisiones hasta la versión RTM del producto o hasta la última revisión de actualización principal. Esta propiedad está disponible a partir de Windows Installer 3,1.
<blockquote>
[!Note]<br />
Para requerir la instalación de Windows Installer 3,1 para aplicar la revisión, establezca la propiedad MinimumRequiredMsiVersion en 310 en la <a href="properties-table-patchwiz-dll-.md">tabla de propiedades</a> del archivo. PCP.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>Valor de cadena que contiene el nombre de la aplicación o el conjunto de aplicaciones de destino. Esta propiedad es obligatoria.</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>Valor de cadena que contiene una dirección URL que apunta a la información de esta revisión. Esta propiedad obligatoria está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partir de Windows XP con Service Pack 2 (SP2), este valor puede ser el vínculo de soporte técnico de la revisión que se muestra en Agregar o quitar programas.<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>Valor de cadena que contiene la hora de creación del archivo. MSP con el formato MM-DD-YY HH: MM (mes-día-año hora: minuto). Esta propiedad es opcional.</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>Valor de cadena que contiene el título de la revisión que es adecuado para la presentación pública. Esta propiedad es obligatoria. Esta propiedad está registrada y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> . A partir de Windows XP con SP2, este valor es el nombre de la revisión que se muestra en Agregar o quitar programas a partir de Windows XP con SP2.<br/></td>
</tr>
<tr class="even">
<td>Descripción</td>
<td>Valor de cadena que contiene una breve descripción de la revisión. Esta propiedad es obligatoria.</td>
</tr>
<tr class="odd">
<td>Clasificación</td>
<td>Valor de cadena que contiene la categoría arbitraria de actualizaciones tal como la define el autor de la revisión. Por ejemplo, los autores de revisiones pueden especificar que cada revisión se clasifique como revisión, acumulación de seguridad, actualización crítica, actualización, Service Pack o paquete acumulativo de actualizaciones. Esta propiedad es obligatoria.</td>
</tr>
<tr class="even">
<td>OptimizedInstallMode</td>
<td>Si esta propiedad se establece en 1 (uno) en todas las revisiones que se van a aplicar en una transacción, la aplicación de la revisión se optimizará si es posible. Para obtener más información, vea <a href="patch-optimization.md">optimización de revisiones</a>. Disponible a partir de Windows Installer 3,1.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de la propiedad de metadatos. Nunca puede ser null ni una cadena vacía. Este valor se puede localizar.

</dd> </dl>

### <a name="remarks"></a>Observaciones

Disponible a partir de Windows Installer 3,0.

Todas las propiedades creadas en la tabla PatchMetadata se agregan a la tabla MsiPatchMetadata del archivo MSP. Las propiedades AllowRemoval, MoreInfoURL y DisplayName se registran y son accesibles a través de [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).

 

 





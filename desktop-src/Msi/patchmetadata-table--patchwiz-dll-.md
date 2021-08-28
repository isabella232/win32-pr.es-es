---
description: La tabla PatchMetadata contiene información sobre una revisión de Windows Installer necesaria para quitar una revisión y que se usa en Agregar o quitar programas.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabla PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af760fbe286cf37cdb3aefe389ee8d09d7a759d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475451"
---
# <a name="patchmetadata-table-patchwizdll"></a>Tabla PatchMetadata (PATCHWIZ.DLL)

La tabla PatchMetadata contiene información sobre una revisión de Windows Installer necesaria para quitar una revisión y que se usa en Agregar o quitar programas. Todas las propiedades de la tabla PatchMetadata se agregan a la tabla [MsiPatchMetadata](msipatchmetadata-table.md) del archivo .msp para una revisión.

La tabla PatchMetadata es necesaria en los archivos de propiedades de creación de revisiones (archivos .cro) que tienen un Valor MínimoRequiredMsiVersion igual a 300 en la tabla [de propiedades](properties-table-patchwiz-dll-.md). La tabla es opcional si MinimumRequiredMsiVersion no es igual a 300.

La tabla PatchMetadata tiene las columnas siguientes.



| Columna   | Tipo | Clave | Nullable |
|----------|------|-----|----------|
| Compañía  | texto | Y   | Y        |
| Propiedad | texto | Y   | No        |
| Valor    | texto |     | Y        |



 

### <a name="columns"></a>Columnas

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Empresa
</dt> <dd>

Nombre de la empresa. Un campo vacío (un valor NULL) indica que esta fila contiene una de las propiedades de metadatos estándar. Una empresa puede extender el conjunto de propiedades agregando una fila a la tabla y especificando un nombre de empresa en este campo.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Nombre de una propiedad de metadatos. Las propiedades AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description y Classification son necesarias en la tabla PatchMetadata . Este campo debe contener una de las siguientes propiedades de metadatos estándar si el campo Company está vacío (un valor NULL).




| Propiedad | Descripción | 
|----------|-------------|
| AllowRemoval | Valor entero que indica si la revisión es o no <a href="uninstallable-patches.md">una revisión que se puede desinstalar.</a> Si el campo Valor contiene un valor 0 (cero), no se puede quitar la revisión. Si el campo Valor contiene 1 (uno), la revisión es una revisión desinstalable. Esta propiedad es obligatoria. Esta propiedad está registrada y su valor se puede obtener mediante la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>función MsiGetPatchInfoEx.</strong></a><br /> | 
| ManufacturerName | Valor de cadena que contiene el nombre del fabricante de la aplicación. Esta propiedad es obligatoria. | 
| MinorUpdateTargetRTM | Indica que la revisión tiene como destino la versión RTM del producto o la revisión de actualización principal más reciente. Cree esta propiedad opcional en revisiones de actualización secundarias que contengan información de secuenciación para indicar que la revisión quita todas las revisiones hasta la versión RTM del producto o hasta la revisión de actualización principal más reciente. Esta propiedad está disponible a partir de Windows Installer 3.1.<blockquote>[!Note]<br />Para requerir que Windows Installer 3.1 esté instalado para aplicar la revisión, establezca la propiedad MinimumRequiredMsiVersion en 310 en la tabla Properties del archivo .debian. <a href="properties-table-patchwiz-dll-.md"></a></blockquote><br /><br /> | 
| TargetProductName | Valor de cadena que contiene el nombre de la aplicación o del conjunto de aplicaciones de destino. Esta propiedad es obligatoria. | 
| MoreInfoURL | Valor de cadena que contiene una dirección URL que apunta a la información de esta revisión. Esta propiedad necesaria está registrada y su valor se puede obtener mediante la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>función MsiGetPatchInfoEx.</strong></a> A partir Windows XP con Service Pack 2 (SP2), este valor puede ser el vínculo de soporte técnico para la revisión que se muestra en Agregar o quitar programas.<br /> | 
| CreationTimeUTC | Valor de cadena que contiene la hora de creación del archivo .msp con el formato mm-dd-yy HH:MM (month-day-year hour:minute). Esta propiedad es opcional. | 
| DisplayName | Valor de cadena que contiene el título de la revisión que es adecuado para la presentación pública. Esta propiedad es obligatoria. Esta propiedad está registrada y su valor se puede obtener mediante la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>función MsiGetPatchInfoEx.</strong></a> A partir Windows XP con SP2, este valor es el nombre de la revisión que se muestra en Agregar o quitar programas a partir de Windows XP con SP2.<br /> | 
| Descripción | Valor de cadena que contiene una breve descripción de la revisión. Esta propiedad es obligatoria. | 
| Clasificación | Valor de cadena que contiene la categoría arbitraria de actualizaciones definida por el autor de la revisión. Por ejemplo, los autores de revisiones pueden especificar que cada revisión se clasifique como revisión, acumulación de seguridad, actualización crítica, actualización, Service Pack o paquete acumulativo de actualizaciones. Esta propiedad es obligatoria. | 
| OptimizedInstallMode | Si esta propiedad se establece en 1 (una) en todas las revisiones que se aplicarán en una transacción, la aplicación de la revisión se optimiza si es posible. Para obtener información, vea <a href="patch-optimization.md">Optimización de revisiones.</a> Disponible a partir Windows Installer 3.1. | 




 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de la propiedad de metadatos. Nunca puede ser Null o una cadena vacía. Este valor se puede localizar.

</dd> </dl>

### <a name="remarks"></a>Comentarios

Disponible a partir de Windows Installer 3.0.

Todas las propiedades que se crearon en la tabla PatchMetadata se agregan a la tabla MsiPatchMetadata del archivo msp. Las propiedades AllowRemoval, MoreInfoURL y DisplayName están registradas y son accesibles a través de [**MsiGetPatchInfoEx.**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)

 

 





---
description: La tabla MsiPatchMetadata contiene información sobre una revisión de Windows Installer que es necesaria para quitar la revisión y que usa Agregar o quitar programas.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabla MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee71e25bf04a39d8d360c5977fad7ec72a8924b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169789"
---
# <a name="msipatchmetadata-table"></a>Tabla MsiPatchMetadata

La tabla MsiPatchMetadata contiene información sobre una revisión de Windows Installer que es necesaria para quitar la revisión y que usa **Agregar o quitar programas.**

Las revisiones instaladas sin esta tabla presente en la base de datos de revisión (archivo .msp) no se pueden quitar y faltan cierta información de **Agregar o quitar programas.** La tabla debe estar en la base de datos del archivo de revisión y no en una transformación de la revisión.

La tabla MsiPatchMetadata tiene las columnas siguientes.



| Columna   | Tipo                         | Clave | Nullable |
|----------|------------------------------|-----|----------|
| Compañía  | [Identificador](identifier.md) | Y   | Y        |
| Propiedad | [Identificador](identifier.md) | Y   | No        |
| Value    | [Texto](text.md)             | No   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Empresa
</dt> <dd>

Nombre de la empresa. Un campo vacío (un valor NULL) indica que la fila contiene una de las propiedades de metadatos estándar del Windows instalador. Para obtener más información, vea la sección Comentarios de este tema.

Al agregar una fila a la tabla y escribir un nombre de empresa en este campo, puede agregar cualquier empresa para ampliar el conjunto de propiedades.

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propiedad
</dt> <dd>

Nombre de una propiedad de metadatos.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor de propiedad de los metadatos. Nunca puede ser Null o una cadena vacía.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Disponible en Windows Installer 3.0 y versiones posteriores.

Las filas de la tabla MsiPatchMetadata que contienen un valor NULL en el campo CompanyName hacen referencia a una de las siguientes propiedades estándar de metadatos Windows Installer.




| Propiedad | Descripción | 
|----------|-------------|
| AllowRemoval | Indica si la revisión es o no <a href="uninstallable-patches.md">una revisión desinstalable.</a> Si el campo de valor contiene 0 (cero), no se puede quitar la revisión. Si el campo de valor contiene uno (1), la revisión es una revisión que se puede desinstalar. Esta propiedad se registra y su valor se puede obtener mediante la función <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx.</strong></a> <br /> | 
| ManufacturerName | Nombre del fabricante de la aplicación. | 
| MinorUpdateTargetRTM | Indica que la revisión tiene como destino la versión RTM del producto o la revisión de actualización principal más reciente. Cree esta propiedad opcional en revisiones de actualización secundarias que contengan información de secuenciación para indicar que la revisión quita todas las revisiones hasta la versión RTM del producto o hasta la revisión de actualización principal más reciente. Esta propiedad está disponible en Windows Installer 3.1 y versiones posteriores. <br /> | 
| TargetProductName | Nombre de la aplicación o conjunto de aplicaciones de destino. | 
| MoreInfoURL | Dirección URL que proporciona información específica de esta revisión. Esta propiedad está registrada y su valor se puede obtener mediante la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>función MsiGetPatchInfoEx.</strong></a> A partir Windows XP con Service Pack 2 (SP2), este valor puede ser el vínculo de soporte técnico de la revisión que se muestra <strong>en Agregar o quitar programas</strong>.<br /> | 
| CreationTimeUTC | Hora de creación del archivo .msp en forma de mm-dd-yy HH:MM (month-day-year hour:minute). | 
| DisplayName | Título de la revisión que es correcto para la presentación pública. Esta propiedad está registrada y su valor se puede obtener mediante la <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>función MsiGetPatchInfoEx.</strong></a> A partir Windows XP con SP2, este valor es el nombre de la revisión que se muestra en <strong>Agregar o quitar programas</strong>.<br /> | 
| Descripción | Breve descripción de la revisión. | 
| clasificación | Valor de cadena que contiene la categoría arbitraria de actualizaciones definida por el autor de la revisión. Por ejemplo, los autores de revisiones pueden especificar que cada revisión se clasifique como revisión, acumulación de seguridad, actualización crítica, actualización, Service Pack o paquete acumulativo de actualizaciones. Esta propiedad es obligatoria. | 
| OptimizeCA | Indica si el instalador Windows omitir las acciones personalizadas al aplicar la revisión. Esto puede reducir el tiempo necesario para aplicar la revisión. La propiedad OptimizeCA puede tener uno de los siguientes valores:<br /><ul><li>0: no omita ninguna acción personalizada.</li><li>1 - Omitir acciones personalizadas de asignación de directorios y propiedades. <a href="custom-action-type-35.md">Custom Action Type 35 (Tipo de acción personalizada 35)</a> y Custom Action Type 51 (Tipo de acción personalizada <a href="custom-action-type-51.md">51)</a> pueden ser acciones personalizadas de asignación de directorios y propiedades.</li><li>2 - Omita las acciones personalizadas inmediatas que no entran en las asignaciones de propiedades o directorios. Las acciones personalizadas inmediatas no incluyen la opción msidbCustomActionTypeInScript en la columna Type de <a href="customaction-table.md">la tabla CustomAction</a>.</li><li>4 - Omita las acciones personalizadas que se ejecutan dentro del script.</li></ul>El valor de OptimizeCA debe ser el mismo para todas las revisiones que se están instalando o no se omite ninguna acción personalizada. Por ejemplo, si se instalan dos revisiones y OptimizeCA se establece en los valores 1 y 2 respectivamente, no se omite ninguna acción personalizada. <br /> Los valores de OptimizeCA se pueden combinar al procesar varias revisiones nuevas. Si todas las revisiones tienen un 1 (uno) incluido en los valores, se omiten todas las acciones personalizadas de asignación de propiedades y directorios. Si una revisión tiene el valor 3 (tres) para la propiedad y una revisión tiene el valor 1 (uno) para la propiedad , se omiten las acciones personalizadas de asignación de propiedades y directorios. Sin embargo, se ejecutan las demás acciones personalizadas inmediatas, porque no se omiten todas las revisiones solicitadas. <br /> | 
| OptimizedInstallMode | Si esta propiedad se establece en 1 (una) en todas las revisiones que se aplicarán en una transacción, se optimiza una aplicación de la revisión si es posible. Para obtener más información, vea <a href="patch-optimization.md">Optimización de revisiones.</a> Disponible a partir de Windows Installer 3.1. | 




 

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 





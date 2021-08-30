---
description: La tabla Actualizar contiene la información necesaria durante las actualizaciones principales.
ms.assetid: f5fda405-8a09-495e-aa8c-b808a2f02b0f
title: Actualizar tabla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3085de7bb834e907ce7b5f1edbee388f5e48b5f72489954aacf3d9e85c2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039202"
---
# <a name="upgrade-table"></a>Actualizar tabla

La tabla Upgrade contiene la información necesaria durante [las actualizaciones principales.](major-upgrades.md) Para habilitar completamente las funcionalidades de actualización del instalador, cada paquete debe tener una [**propiedad UpgradeCode**](upgradecode.md) y una tabla Upgrade. Cada registro de la tabla Actualizar proporciona una combinación característica de código de actualización, versión del producto e información de idioma que se usa para identificar un conjunto de productos afectados por la actualización. Cuando la [acción FindRelatedProducts](findrelatedproducts-action.md) detecta un producto afectado instalado en el sistema, anexa el código de producto a una propiedad especificada en la columna ActionProperty. La [acción RemoveExistingProducts](removeexistingproducts-action.md) y [la acción MigrateFeatureStates](migratefeaturestates-action.md) solo quitan o migran los productos enumerados en la columna ActionProperty.

La tabla Upgrade contiene las columnas que se muestran en la tabla siguiente.



| Columna         | Tipo                         | Clave | Nullable |
|----------------|------------------------------|-----|----------|
| UpgradeCode    | [GUID](guid.md)             | Y   | N        |
| VersionMin     | [Texto](text.md)             | Y   | Y        |
| VersionMax     | [Texto](text.md)             | Y   | Y        |
| Lenguaje       | [Texto](text.md)             | Y   | Y        |
| Atributos     | [Entero](integer.md)       | Y   | N        |
| Quitar         | [Formato](formatted.md)   | N   | Y        |
| ActionProperty | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="UpgradeCode"></span><span id="upgradecode"></span><span id="UPGRADECODE"></span>UpgradeCode
</dt> <dd>

La [propiedad UpgradeCode](upgradecode.md) de esta columna especifica el código de actualización de todos los productos que va a detectar [la acción FindRelatedProducts.](findrelatedproducts-action.md)

</dd> <dt>

<span id="VersionMin"></span><span id="versionmin"></span><span id="VERSIONMIN"></span>VersionMin
</dt> <dd>

Límite inferior del intervalo de versiones de producto detectado por [FindRelatedProducts.](findrelatedproducts-action.md) Escriba **msidbUpgradeAttributesVersionMinInclusive** en Atributos para incluir VersionMin en el intervalo. Si VersionMin es igual a una cadena vacía ("") se evalúa igual que 0. Si VersionMin es null, FindRelatedProducts omite **msidbUpgradeAttributesVersionMinInclusive** y detecta todas las versiones anteriores. VersionMin y VersionMax no deben ser null.

VersionMin debe ser una versión válida del producto como se describe para la [**propiedad ProductVersion.**](productversion.md) Tenga en cuenta Windows instalador usa solo los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

</dd> <dt>

<span id="VersionMax"></span><span id="versionmax"></span><span id="VERSIONMAX"></span>VersionMax
</dt> <dd>

Límite superior del intervalo de versiones de producto detectado por la [acción FindRelatedProducts.](findrelatedproducts-action.md) Escriba **msidbUpgradeAttributesVersionMaxInclusive** en Atributos para incluir VersionMax en el intervalo. Si VersionMax es una cadena vacía (""), se evalúa igual que 0. Si VersionMax es null, FindRelatedProducts omite **msidbUpgradeAttributesVersionMaxInclusive** y detecta todas las versiones del producto mayores (o mayores o iguales que) el límite inferior especificado por VersionMin y **msidbUpgradeAttributesVersionMinInclusive**. VersionMin y VersionMax no deben ser null.

VersionMax debe ser una versión de producto válida como se describe para la [**propiedad ProductVersion.**](productversion.md) Tenga en cuenta Windows instalador usa solo los tres primeros campos de la versión del producto. Si incluye un cuarto campo en la versión del producto, el instalador omite el cuarto campo.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lengua
</dt> <dd>

Conjunto de idiomas detectados [por FindRelatedProducts.](findrelatedproducts-action.md) Escriba una lista de identificadores numéricos de idioma (LANGID) separados por comas. Escriba **msidbUpgradeAttributesLanguagesExclusive** en Atributos para detectar todos los idiomas exclusivos de los enumerados en Idioma. Si Language es null o una cadena vacía (""), FindRelatedProducts omite **msidbUpgradeAttributesLanguagesExclusive** y detecta todos los idiomas.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Esta columna contiene marcas de bits que especifican los atributos de la tabla Upgrade.



| Nombre de la marca de bits                                 | Decimal | Hexadecimal | Atributo                                                                                                            |
|-----------------------------------------------|---------|-------------|----------------------------------------------------------------------------------------------------------------------|
| **msidbUpgradeAttributesMigrateFeatures**     | 1       | 0x001       | Migra los estados de características habilitando la lógica en [la acción MigrateFeatureStates.](migratefeaturestates-action.md) |
| **msidbUpgradeAttributesOnlyDetect**          | 2       | 0x002       | Detecta productos y aplicaciones, pero no lo quita.                                                               |
| **msidbUpgradeAttributesIgnoreRemoveFailure** | 4       | 0x004       | Continúa la instalación en caso de error al quitar un producto o una aplicación.                                              |
| **msidbUpgradeAttributesVersionMinInclusive** | 256     | 0x100       | Detecta el intervalo de versiones, incluido el valor de VersionMin.                                                     |
| **msidbUpgradeAttributesVersionMaxInclusive** | 512     | 0x200       | Detecta el intervalo de versiones, incluido el valor de VersionMax.                                                     |
| **msidbUpgradeAttributesLanguagesExclusive**  | 1024    | 0x400       | Detecta todos los idiomas, excepto los idiomas enumerados en la columna Idioma.                                        |



 

</dd> <dt>

<span id="Remove"></span><span id="remove"></span><span id="REMOVE"></span>eliminar
</dt> <dd>

El instalador establece la [**propiedad REMOVE**](remove.md) en las características especificadas en esta columna. Las características que se quitarán se pueden determinar en tiempo de ejecución. La [cadena con formato](formatted.md) especificada en este campo debe evaluarse como una lista delimitada por comas de nombres de características. Por ejemplo: \[ Feature1 \] , \[ Feature2 \] , \[ Feature3 \] . No se quita ninguna características si el campo contiene texto con formato que se evalúa como una cadena vacía (""). El instalador establece REMOVE=ALL solo si el campo Quitar está vacío. Observe la diferencia entre una cadena vacía y un campo vacío. Si el campo está vacío, es null.

</dd> <dt>

<span id="ActionProperty"></span><span id="actionproperty"></span><span id="ACTIONPROPERTY"></span>ActionProperty
</dt> <dd>

Cuando la [acción FindRelatedProducts](findrelatedproducts-action.md) detecta un producto relacionado instalado en el sistema, anexa el código de producto a la propiedad especificada en este campo. La propiedad especificada en esta columna debe ser una propiedad pública y el autor del paquete debe agregar la propiedad a la [**propiedad SecureCustomProperties.**](securecustomproperties.md) Cada fila de la tabla Upgrade debe tener un valor ActionProperty único. Después de FindRelatedProducts, el valor de esta propiedad es una lista de códigos de producto, separados por punto y coma (;), detectados en el sistema.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE61](ice61.md)  
[ICE66](ice66.md)  
</dl>

 

 




---
description: La tabla TargetImages contiene información sobre las imágenes de destino del producto. Un Windows de revisión del instalador actualiza una imagen de destino en una imagen actualizada.
ms.assetid: 4681715e-9918-4d7b-8f33-1cca2bb34eb7
title: Tabla TargetImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbb8e7bae92fbc25b217808aaae709f079d65dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069615"
---
# <a name="targetimages-table-patchwizdll"></a>Tabla TargetImages (Patchwiz.dll)

La tabla TargetImages contiene información sobre las imágenes de destino del producto. Un Windows de revisión del instalador actualiza una imagen de destino en una imagen actualizada.

Se requiere una tabla TargetImages que contenga al menos un registro en cada base de datos de creación de revisiones (archivo .csv). La función [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) usa esta tabla.

La tabla TargetImages tiene las columnas siguientes.



| Columna                | Tipo    | Clave | Nullable |
|-----------------------|---------|-----|----------|
| Destino                | text    | Y   | N        |
| MsiPath               | text    |     | N        |
| SymbolPaths           | text    |     | Y        |
| Upgraded              | text    |     | N        |
| Pedido                 | integer |     | N        |
| ProductValidateFlags  | text    |     | Y        |
| IgnoreMissingSrcFiles | integer |     | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Objetivo
</dt> <dd>

Identificador de una imagen de destino. El paquete de revisión actualiza la imagen de destino especificada en esta columna a la imagen actualizada especificada en la columna Actualizado. Hay una o varias imágenes de destino para cada imagen actualizada. La imagen de destino debe ser una imagen de configuración completamente sin comprimir del producto, como una imagen administrativa o una imagen de configuración sin comprimir en un CD-ROM. Tenga en cuenta [que la función UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) no genera revisiones binarias para los archivos de los archivadores. El valor de este campo se usa con el valor del campo Actualizado para generar los nombres de las transformaciones que el instalador agrega al paquete de revisión.

</dd> <dt>

<span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath
</dt> <dd>

Este campo especifica la ruta de acceso completa, incluido el nombre de archivo, a la ubicación del archivo .msi para la imagen de destino. Esta es la ubicación de los archivos de origen de la imagen de destino.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Lista delimitada por punto y coma de carpetas en las que se van a buscar archivos de símbolos que se pueden usar para optimizar la generación de la revisión binaria. Tenga en cuenta que no se buscan los subdirectorios de las carpetas especificadas en este campo. Una revisión binaria optimizada puede ser más pequeña. Microsoft Visual C++ debe instalarse en el equipo que genera la revisión y usarse para crear los archivos de símbolos. Este campo es opcional y el instalador crea una revisión binaria incluso si no se especifica ningún archivo de símbolos o si los archivos de símbolos no están disponibles para Patchwiz.dll.

</dd> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Actualizado
</dt> <dd>

Clave externa a la columna Actualizado de [la tabla UpgradedImages](upgradedimages-table-patchwiz-dll-.md). La [función UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) omite cualquier imagen actualizada a la que no haga referencia al menos un registro de la tabla TargetImages.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Orden
</dt> <dd>

Orden relativo de la imagen de destino. Dado que se pueden aplicar revisiones a varios destinos a una imagen actualizada, el campo Order proporciona un medio para secuenciar las transformaciones en la lista de transformaciones de revisión. Normalmente, el orden va de la imagen más antigua a la más reciente.

</dd> <dt>

<span id="ProductValidateFlags"></span><span id="productvalidateflags"></span><span id="PRODUCTVALIDATEFLAGS"></span>ProductValidateFlags
</dt> <dd>

El campo ProductValidateFlags se usa para especificar la comprobación del producto para evitar aplicar transformaciones irrelevantes. El valor especificado en este campo debe ser un entero hexadecimal de 8 dígitos y uno de los valores válidos para el parámetro *iValidation* de la función [**MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) El valor predeterminado es 0x00000922 que es igual a **MSITRANSFORM \_ VALIDATE \_ UPDATEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ NEWEQUALBASEVERSION**  +  **MSITRANSFORM \_ VALIDATE \_ UPGRADECODE**  +  **MSITRANSFORM \_ VALIDATE \_ PRODUCT**.

</dd> <dt>

<span id="IgnoreMissingSrcFiles"></span><span id="ignoremissingsrcfiles"></span><span id="IGNOREMISSINGSRCFILES"></span>IgnoreMissingSrcFiles
</dt> <dd>

Si este campo se establece en un valor distinto de cero, el instalador omite los archivos que faltan en la imagen de destino y no se modifican durante la aplicación de revisiones. Esto permite realizar revisiones sin necesidad de toda la imagen. solo se requieren los archivos modificados del producto y .msi archivo. Esto puede reducir el tiempo necesario para generar la revisión.

> [!Note]  
> No use el valor IgnoreMissingSrcFiles con TrustMsi establecido en 1 en la [tabla Properties](properties-table-patchwiz-dll-.md).

 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla acepta variables de entorno como rutas de acceso a partir de la versión 4.0 de Patchwiz.dll.

 

 




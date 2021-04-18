---
description: ICE80 valida que el valor de la propiedad de Resumen de plantilla ( \_ plantilla de PID) especifique correctamente &\# 0034; Intel64&\# 0034;, &\# 0034; x64&\# 0034; o &\# 0034; Intel&\# 0034; según la presencia de componentes de 64 bits o scripts de acción personalizados.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5233f260e9cc248bdb2d0c19b47956a2b7dbe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652464"
---
# <a name="ice80"></a>ICE80

ICE80 valida que el valor de la propiedad de [**Resumen de plantilla**](template-summary.md) (plantilla de PID \_ ) especifique correctamente "Intel64", "x64", "Arm64" o "Intel" dependiendo de la presencia de componentes de 64 bits o scripts de acción personalizados. ICE80 comprueba la [tabla](component-table.md) de componentes de los componentes con el atributo **msidbComponentAttributes64bit** y comprueba la [tabla CustomAction](customaction-table.md) en busca de cualquier script con el atributo **msidbCustomActionType64BitScript** . ICE80 comprueba que un paquete con "Intel64", "x64" o "Arm64" en la propiedad de **Resumen** de la plantilla también tiene una propiedad de [**Resumen de recuento de páginas**](page-count-summary.md) (PID \_ PAGECOUNT) de al menos 150.

ICE80 también valida que el identificador de idioma especificado por la propiedad [**ProductLanguage**](productlanguage.md) debe estar incluido en la propiedad de Resumen de la [**plantilla**](template-summary.md) .

Para obtener más información, consulte [Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md).

## <a name="result"></a>Resultado

ICE80 expone los siguientes errores.



| Error                                                                                                                                                                   | Descripción                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Este paquete contiene el componente de 64 bits ' \[ 1 \] ', pero la propiedad de [**Resumen**](template-summary.md) de la plantilla no contiene Intel64, x64 o Arm64.                    | La [tabla de componentes](component-table.md)contiene un componente con el atributo **msidbComponentAttributes64bit** y la propiedad de Resumen de la [**plantilla**](template-summary.md) no contiene Intel64, x64 o Arm64.        |
| Este paquete contiene el script de acción personalizada de 64 bits ' \[ 1 \] ', pero la propiedad de [**Resumen**](template-summary.md) de la plantilla no contiene Intel64, x64 o Arm64.         | La [tabla CustomAction](customaction-table.md) contiene una acción personalizada de script con **msidbCustomActionType64BitScript** , pero la propiedad de Resumen de la [**plantilla**](template-summary.md) no contiene Intel64, x64 o Arm64. |
| Valor incorrecto en el flujo de información de resumen para% s.                                                                                                                         | Se devuelve para \_ la propiedad de plantilla de PID si esa propiedad es una cadena vacía o no es un tipo de VT \_ LPSTR. Se devuelve para \_ el PID PAGECOUNT si esa propiedad no es un tipo de tipo de error VT \_ .<br/>                                         |
| Este paquete está marcado con Intel64 pero tiene un esquema inferior a 150.                                                                                                  | La \_ propiedad de plantilla de PID del paquete es Intel64, pero su \_ propiedad de PID PAGECOUNT es inferior a 150.                                                                                                            |
| Este paquete está marcado con x64, pero tiene un esquema inferior a 200.                                                                                                      | La \_ propiedad de plantilla de PID del paquete es x64, pero su \_ propiedad de PID PAGECOUNT es inferior a 200.                                                                                                            |
| Este paquete está marcado con Arm64 pero tiene un esquema inferior a 500.                                                                                                    | La \_ propiedad de plantilla de PID del paquete es Arm64, pero su \_ propiedad de PID PAGECOUNT es inferior a 500.                                                                                                            |
| Este paquete de 32 bits está utilizando la propiedad 1 de 64 bits \[\]                                                                                                                       | Un paquete de 32 bits está usando una propiedad de 64 bits.                                                                                                                                                                              |
| Este paquete de 32 bits usa el tipo de localizador de 64 bits en la entrada de la tabla RegLocator \[ 1\]                                                                                         | Un paquete de 32 bits contiene **msidbLocatorType64bit** en el campo Type de la [tabla RegLocator](reglocator-table.md).                                                                                                    |
| Este 64BitComponent \[ 1 \] usa 32BitDirectory \[ 3\]                                                                                                                     | Un componente de 64 bits está utilizando un directorio de 32 bits.                                                                                                                                                                           |
| Este 32BitComponent \[ 1 \] usa 64BitDirectory \[ 3\]                                                                                                                     | Un componente de 32 bits está utilizando un directorio de 64 bits.                                                                                                                                                                           |
| La propiedad '[**ProductLanguage**](productlanguage.md)' de la tabla de propiedades tiene un valor de ' \[ 2 \] ', que no se incluye en la secuencia de propiedades de Resumen de la plantilla. | El valor de la propiedad [**ProductLanguage**](productlanguage.md) no aparece en la lista de propiedades de Resumen de la [**plantilla**](template-summary.md) .                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> <dt>

[Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 





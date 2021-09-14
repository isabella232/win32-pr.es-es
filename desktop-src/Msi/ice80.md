---
description: ICE80 valida que el valor de la propiedad Template Summary (PID TEMPLATE) especifica correctamente \_ &\# 0034;Intel64&\# 0034;, &\# 0034;x64&\# 0034; o &\# 0034;Intel&\# 0034; en función de la presencia de componentes de 64 bits o scripts de acción personalizados.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5233f260e9cc248bdb2d0c19b47956a2b7dbe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074533"
---
# <a name="ice80"></a>ICE80

ICE80 valida que el [](template-summary.md) valor de la propiedad Resumen de plantilla (PID TEMPLATE) especifica correctamente \_ "Intel64", "x64", "Arm64" o "Intel" en función de la presencia de componentes de 64 bits o scripts de acción personalizados. ICE80 comprueba [](component-table.md) en la tabla de componentes los componentes con el atributo **msidbComponentAttributes64bit** y comprueba en la [tabla CustomAction](customaction-table.md) los scripts con el atributo **msidbCustomActionType64BitScript.** ICE80 comprueba que un paquete con "Intel64", "x64" o  "Arm64" en [](page-count-summary.md) su propiedad Resumen de plantilla también tiene una propiedad resumen de recuento de páginas (PID PAGECOUNT) de al menos \_ 150.

ICE80 también valida que el identificador de idioma especificado por la [**propiedad ProductLanguage**](productlanguage.md) debe estar incluido en la [**propiedad Resumen de**](template-summary.md) plantilla.

Para obtener más información, [vea Windows Installer en sistemas operativos de 64 bits.](windows-installer-on-64-bit-operating-systems.md)

## <a name="result"></a>Resultado

ICE80 publica los siguientes errores.



| Error                                                                                                                                                                   | Descripción                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Este paquete contiene el componente de 64 bits '1', pero la propiedad Resumen de plantilla no contiene \[ \] Intel64, x64 ni Arm64. [](template-summary.md)                    | La [tabla de componentes](component-table.md)contiene un componente con el atributo **msidbComponentAttributes64bit** y la propiedad [**Resumen**](template-summary.md) de plantilla no contiene Intel64, x64 ni Arm64.        |
| Este paquete contiene el script de acción personalizada de 64 bits '1', pero la propiedad Resumen de plantilla no contiene \[ \] Intel64, x64 ni Arm64. [](template-summary.md)         | [La tabla CustomAction](customaction-table.md) contiene una acción personalizada de script con **msidbCustomActionType64BitScript,** pero la propiedad [**Resumen**](template-summary.md) de plantilla no contiene Intel64, x64 ni Arm64. |
| Valor no válido en Secuencia de información de resumen para %s.                                                                                                                         | Se devuelve para \_ la propiedad PID TEMPLATE si esa propiedad es una cadena vacía o no un tipo \_ LPSTR de VT. Se devuelve para PID \_ PAGECOUNT si esa propiedad no es un tipo VT \_ I4.<br/>                                         |
| Este paquete está marcado con Intel64, pero tiene un esquema menor que 150.                                                                                                  | La propiedad \_ PID TEMPLATE del paquete es Intel64, pero su propiedad PAGECOUNT de PID es menor que \_ 150.                                                                                                            |
| Este paquete está marcado con x64, pero tiene un esquema menor que 200.                                                                                                      | La propiedad \_ PID TEMPLATE del paquete es x64, pero su propiedad PAGECOUNT de PID es menor que \_ 200.                                                                                                            |
| Este paquete está marcado con Arm64, pero tiene un esquema menor que 500.                                                                                                    | La propiedad \_ PID TEMPLATE del paquete es Arm64, pero su propiedad PAGECOUNT de PID es menor que \_ 500.                                                                                                            |
| Este paquete de 32 bits usa la propiedad 1 de 64 bits \[\]                                                                                                                       | Un paquete de 32 bits usa una propiedad de 64 bits.                                                                                                                                                                              |
| Este paquete de 32 bits usa el tipo de localizador de 64 bits en la entrada 1 de la tabla RegLocator \[\]                                                                                         | Un paquete de 32 bits contiene **msidbLocatorType64bit** en el campo Type de la [tabla RegLocator](reglocator-table.md).                                                                                                    |
| Este 64BitComponent \[ 1 \] usa 32BitDirectory \[ 3\]                                                                                                                     | Un componente de 64 bits usa un directorio de 32 bits.                                                                                                                                                                           |
| Este 32BitComponent \[ 1 \] usa 64BitDirectory \[ 3\]                                                                                                                     | Un componente de 32 bits usa un directorio de 64 bits.                                                                                                                                                                           |
| La propiedad [**' ProductLanguage**](productlanguage.md)' de la tabla Property tiene un valor de '2', que no se encuentra en el flujo de la propiedad \[ \] Template Summary. | El valor de la [**propiedad ProductLanguage**](productlanguage.md) no aparece en la [**propiedad Resumen de**](template-summary.md) plantilla.                                                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> <dt>

[Windows Instalador en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 





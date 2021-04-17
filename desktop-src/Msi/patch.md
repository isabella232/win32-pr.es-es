---
description: El instalador establece la propiedad PATCH en una lista de revisiones que se aplican mediante una llamada a MsiApplyPatch, MsiApplyMultiplePatches o la opción de línea de comandos/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: PATCH (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653843"
---
# <a name="patch-property"></a>PATCH (propiedad)

El instalador establece la propiedad **patch** en una lista de revisiones que se aplican mediante una llamada a [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) o la opción de [línea de comandos](command-line-options.md)/p. También puede establecer la propiedad **patch** en la línea de comandos mientras instala un paquete mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o la opción de línea de comandos/i.

El valor de la propiedad **patch** es una lista de las revisiones que se están instalando. Cada revisión de la lista se representa mediante la ruta de acceso completa al paquete de la revisión (archivo. msp). Las rutas de acceso completas de la lista se separan mediante signos de punto y coma.

**Windows Installer 2,0:** No se admiten varias revisiones. Windows Installer 3,0 es necesario para aplicar varias revisiones.

## <a name="remarks"></a>Observaciones

Si crea un paquete de revisión mediante [Msimsp.exe](msimsp-exe.md) y [Patchwiz.dll](patchwiz-dll.md) puede especificar que una acción o un cuadro de diálogo solo se ejecuten cuando se aplique una revisión determinada. Al crear el paquete de revisión, por ejemplo test. MSP, puede crear una imagen actualizada del producto y un archivo de propiedades de creación de revisiones. Al crear el archivo de propiedades de creación de revisiones, puede escribir un nombre de propiedad, por ejemplo PATCHFORTEST, en el campo MediaSrcPropName de la tabla [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) . Al crear las tablas de secuencia de la imagen actualizada del producto, puede incluir en la columna condición de la tabla de secuencia una instrucción condicional para la acción o el cuadro de diálogo que desea hacer condicional.

Por ejemplo, puede usar la siguiente instrucción condicional para ejecutar una acción o un cuadro de diálogo solo cuando se está aplicando test. msp.

<dl> PATCH Y PATCHFORTEST Y PATCH >< PATCHFORTEST  
</dl>

> [!Note]  
> Dado que la propiedad **patch** puede contener varias revisiones, use el operador de subcadena "><" para comprobar la presencia de una revisión determinada en lugar del operador Equals "=". Para obtener más información sobre las instrucciones condicionales, vea la sección [Sintaxis de instrucciones condicionales](conditional-statement-syntax.md) .

 

El instalador establece ambas propiedades si se aplica una lista de revisiones que incluye test. msp. Por ejemplo, puede usar la opción de [línea de comandos](command-line-options.md) /p para aplicar una lista de dos revisiones.

**msiexec/QB/p \\ \\ Scratch \\ Scratch \\ XYZ \\ patches \\ . MSP; \\ \\ Scratch \\ Scratch \\ XYZ \\ bar. MSP**

El instalador establece las propiedades **patch** y PATCHFORTEST como se indica a continuación.

<dl> REVISIÓN = \\ \\ borrado de las \\ revisiones XYZ de Scratch \\ \\ \\ . MSP; \\ \\ Scratch \\ Scratch \\ XYZ \\ bar. MSP  
PATCHFORTEST = \\ \\ borrado de las \\ revisiones XYZ de Scratch \\ \\ \\ . MSP  
</dl>

En este caso, la condición es TRUE y el cuadro de diálogo o acción condicional anterior se puede ejecutar para cada revisión que se está instalando, test. MSP y bar. msp.

Si no se aplica test. MSP, el instalador no lo incluye en la propiedad **patch** y no establece PATCHFORTEST. En este caso, la condición anterior es falsa y la acción condicional o el cuadro de diálogo no se ejecutan.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
</dt> <dt>

[Ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 





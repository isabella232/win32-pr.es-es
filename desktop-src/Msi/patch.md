---
description: El instalador establece la propiedad PATCH en una lista de revisiones que se aplican mediante una llamada a MsiApplyPatch, MsiApplyMultiplePatches o la opción de línea de comandos /p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Patch, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1938ab76e7250d86f5fa40dd6fc64a9f1341982356ed98924ebdad3abd2f2868
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926275"
---
# <a name="patch-property"></a>Patch, propiedad

El instalador establece la propiedad **PATCH** en una lista de revisiones que se aplican mediante una llamada a [**MsiApplyPatch,**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) o la opción de línea de comandos [/p](command-line-options.md). También puede establecer la propiedad **PATCH** en la línea de comandos al instalar un paquete mediante [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o la opción de línea de comandos /i.

El valor de la **propiedad PATCH** es una lista de las revisiones que se están instalando. Cada revisión de la lista se representa mediante la ruta de acceso completa al paquete de la revisión (archivo .msp). Las rutas de acceso completas de la lista están separadas por punto y coma.

**Windows Installer 2.0:** No se admiten varias revisiones. Windows Se requiere el instalador 3.0 para aplicar varias revisiones.

## <a name="remarks"></a>Comentarios

Si crea un paquete [](msimsp-exe.md) de revisión medianteMsimsp.exey [Patchwiz.dll](patchwiz-dll.md) puede especificar que una acción o un cuadro de diálogo solo se ejecuten cuando se aplica una revisión determinada. Al crear el paquete de revisión, por ejemplo test.msp, se crea una imagen actualizada del producto y un archivo de propiedades de creación de revisiones. Al crear el archivo de propiedades de creación de revisiones, puede escribir un nombre de propiedad, por ejemplo PATCHFORTEST, en el campo MediaSrcPropName de la [tabla ImageFamilies.](imagefamilies-table-patchwiz-dll-.md) Al crear las tablas de secuencia de la imagen actualizada del producto, puede incluir en la columna Condición de la tabla de secuencia una instrucción condicional para la acción o el cuadro de diálogo que desea convertir en condicional.

Por ejemplo, puede usar la siguiente instrucción condicional para ejecutar una acción o un cuadro de diálogo solo cuando se aplica test.msp.

<dl> PATCH Y PATCHFORTEST Y PATCH >< PATCHFORTEST  
</dl>

> [!Note]  
> Dado que **la propiedad PATCH** puede contener varias revisiones, use el operador de subcadena "><" para comprobar la presencia de una revisión determinada en lugar del operador equals "=". Para obtener más información sobre las instrucciones condicionales, vea la [sección Sintaxis de instrucciones](conditional-statement-syntax.md) condicionales.

 

El instalador establece ambas propiedades si aplica una lista de revisiones que incluye test.msp. Por ejemplo, puede usar la opción de línea de comandos [/p](command-line-options.md) para aplicar una lista de dos revisiones.

**msiexec /qb /p \\ \\ scratch xyz \\ \\ \\ patches \\ test.msp; \\ \\ scratch \\ scratch \\ XYZ \\ bar.msp**

El instalador establece las **propiedades PATCH** y PATCHFORTEST como se muestra a continuación.

<dl> PATCH= \\ \\ scratch scratch XYZ \\ \\ \\ Patches \\ test.msp; \\ \\ scratch \\ scratch \\ XYZ \\ bar.msp  
PATCHFORTEST= \\ \\ scratch scratch XYZ \\ \\ \\ Patches \\ test.msp  
</dl>

En este caso, la condición es TRUE y se puede ejecutar la acción condicional o el cuadro de diálogo anterior para cada revisión que se instala, test.msp y bar.msp.

Si no se aplica test.msp, el instalador no lo incluye en la **propiedad PATCH** y no establece PATCHFORTEST. En este caso, la condición anterior es FALSE y la acción condicional o el cuadro de diálogo no se ejecuta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Sintaxis de instrucciones condicionales](conditional-statement-syntax.md)
</dt> <dt>

[Ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 





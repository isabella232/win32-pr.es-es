---
description: El valor de la propiedad REMOVE es una lista de características delimitadas por comas que se van a quitar.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786f5c17b7e2007e568aae6cf7d55eb01cd7bd86f009b80da987d5aac44a424c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430665"
---
# <a name="remove-property"></a>REMOVE, propiedad

El valor de la **propiedad REMOVE** es una lista de características delimitadas por comas que se van a quitar. Las características deben estar presentes en la columna Característica de la [tabla Característica](feature-table.md). Tenga en cuenta que si usa REMOVE=ALL en la línea de comandos, el instalador quita todas las características que tienen un nivel de instalación mayor que 0. En este caso, el instalador no quita las características que tienen un nivel de instalación de 0. Para obtener más información sobre el nivel de instalación de las características, vea [Tabla de características](feature-table.md).

## <a name="remarks"></a>Comentarios

Para determinar si un producto se ha establecido para que se desinstale completamente, un autor del paquete puede usar una expresión condicional para comprobar si REMOVE=ALL. Tenga en cuenta que si el producto se quita estableciendo su característica superior en ausente, es posible que la propiedad **REMOVE** no sea igual a ALL hasta después de [la acción InstallValidate](installvalidate-action.md). Esto significa que cualquier acción personalizada que dependa de REMOVE=ALL debe secuenciarse después de InstallValidate. Para obtener más información, vea también [Acciones de aseimismo para ejecutar durante la eliminación.](conditioning-actions-to-run-during-removal.md) Tenga en cuenta que los nombres de características distinguen mayúsculas de minúsculas.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  **eliminar**
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Reinstalar**](reinstall.md)
6.  [**Anunciar**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica ADDLOCAL=ALL, ADDSOURCE = MyFeature, todas las características se establecen primero en run-local y, a continuación, MyFeature se establece en run-from-source. Si la línea de comandos es ADDSOURCE=ALL, ADDLOCAL=MyFeature, primero MyFeature se establece en run-local y, después, cuando se evalúa ADDSOURCE=ALL, todas las características (incluida MyFeature) se restablecen a run-from-source.

El instalador establece la propiedad [**Preselected**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 





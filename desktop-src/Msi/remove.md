---
description: El valor de la propiedad REMOVE es una lista de características delimitadas por comas que se van a quitar.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653913"
---
# <a name="remove-property"></a>REMOVE, propiedad

El valor de la propiedad **Remove** es una lista de características delimitadas por comas que se van a quitar. Las características deben estar presentes en la columna característica de la [tabla de características](feature-table.md). Tenga en cuenta que si usa REMOVE = ALL en la línea de comandos, el instalador quita todas las características que tengan un nivel de instalación superior a 0. En este caso, el instalador no quita las características que tienen un nivel de instalación de 0. Para obtener más información sobre el nivel de instalación de características, vea [tabla de características](feature-table.md).

## <a name="remarks"></a>Observaciones

Para determinar si se ha configurado un producto para que se desinstale por completo, el autor de un paquete puede usar una expresión condicional para comprobar si se quita = ALL. Tenga en cuenta que si el producto se quita estableciendo su característica superior en ausente, es posible que la propiedad **Remove** no sea igual a toda hasta después de la [acción InstallValidate](installvalidate-action.md). Esto significa que cualquier acción personalizada que dependa de REMOVE = ALL se debe secuenciar después de InstallValidate. Para obtener más información, consulte también [acciones de acondicionamiento para ejecutarse durante la eliminación](conditioning-actions-to-run-during-removal.md). Tenga en cuenta que los nombres de las características distinguen mayúsculas de minúsculas.

El instalador siempre evalúa las siguientes propiedades en el orden siguiente:

1.  [**ADDLOCAL**](addlocal.md)
2.  **RETIRAR**
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**REINSTALAR**](reinstall.md)
6.  [**ANUNCIA**](advertise.md)
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Por ejemplo, si la línea de comandos especifica ADDLOCAL = ALL, ADDSOURCE = función, todas las características se establecen primero en Run-local y, a continuación, se establece la función de ejecución-desde-origen. Si la línea de comandos es ADDSOURCE = ALL, ADDLOCAL = función, First la función se establece en Run-local y, cuando se evalúa ADDSOURCE = ALL, todas las características (incluidas las funciones) se restablecen en Run-from-Source.

El instalador establece la propiedad [**preseleccionada**](preselected.md) en un valor de "1" durante la reanudación de una instalación suspendida o cuando se especifica cualquiera de las propiedades anteriores en la línea de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 





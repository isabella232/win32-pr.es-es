---
description: La acción WriteIniValues escribe la información del archivo. ini que la aplicación necesita escribir en sus archivos. ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Acción WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910666"
---
# <a name="writeinivalues-action"></a>Acción WriteIniValues

La acción WriteIniValues escribe la información del archivo. ini que la aplicación necesita escribir en sus archivos. ini. La escritura de esta información se valida mediante la [tabla de componentes](component-table.md). Se escribe un valor. ini si se ha establecido que el componente correspondiente se instale localmente o se ejecute desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallValidate debe ser anterior a la acción WriteIniValues. Si hay una [acción RemoveIniValues](removeinivalues-action.md) en la secuencia, debe ser anterior a la acción WriteIniValues.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción              |
|-------|-----------------------------------------|
| \[1\] | Identificador del archivo. ini.                |
| \[2\] | clave del archivo. ini en la sección siguiente. |
| \[3\] | Elemento quitado del archivo. ini.            |
| \[4\] | Valor quitado del archivo. ini.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla IniFile](inifile-table.md)
</dt> </dl>

 

 




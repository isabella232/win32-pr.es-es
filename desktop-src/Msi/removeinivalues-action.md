---
description: La acción RemoveIniValues quita la información del archivo. ini especificada para su eliminación en la tabla RemoveIniFile si el componente está configurado para instalarse localmente o ejecutar desde el origen.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Acción RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002971"
---
# <a name="removeinivalues-action"></a>Acción RemoveIniValues

La acción RemoveIniValues quita la información del archivo. ini especificada para su eliminación en la [tabla RemoveIniFile](removeinifile-table.md) si el componente está configurado para instalarse localmente o ejecutar desde el origen. La acción RemoveIniValues quita la información del archivo. ini que se ha asociado a un componente de la [tabla inifile](inifile-table.md). Esta acción también quita la información del archivo. ini si la [acción WriteIniValues](writeinivalues-action.md) escribió la información y el componente está programado para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de la acción RemoveIniValues. Si se usa una acción [WriteIniValues](writeinivalues-action.md) en la secuencia, debe aparecer después de RemoveIniValues.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción    |
|-------|-------------------------------|
| \[1\] | Identificador del archivo. ini.      |
| \[2\] | Una sección de la clave del archivo. ini.     |
| \[3\] | Elemento quitado del archivo. ini.  |
| \[4\] | Valor quitado del archivo. ini. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla RemoveIniFile](removeinifile-table.md)
</dt> <dt>

[Tabla IniFile](inifile-table.md)
</dt> <dt>

[Acción WriteIniValues](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 




---
description: La acción RemoveIniValues quita .ini información de archivo especificada para su eliminación en la tabla RemoveIniFile si el componente está establecido para instalarse localmente o ejecutarse desde el origen.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Acción RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095985165bf6d9629aa0cae67a5b3f7975d817151ac4b04de40a08d5c2bab4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626394"
---
# <a name="removeinivalues-action"></a>Acción RemoveIniValues

La acción RemoveIniValues quita .ini información de archivo especificada para su eliminación en la [tabla RemoveIniFile](removeinifile-table.md) si el componente está establecido para instalarse localmente o ejecutarse desde el origen. La acción RemoveIniValues quita .ini información de archivo asociada a un componente de la [tabla IniFile](inifile-table.md). Esta acción también quita .ini información del archivo si la información la escribió la acción [WriteIniValues](writeinivalues-action.md) y el componente está programado para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de la acción RemoveIniValues. Si se [usa una acción WriteIniValues](writeinivalues-action.md) en la secuencia, debe aparecer después de RemoveIniValues.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción    |
|-------|-------------------------------|
| \[1\] | Identificador de .ini archivo.      |
| \[2\] | Una .ini clave de archivo.     |
| \[3\] | Elemento quitado de .ini archivo.  |
| \[4\] | Valor quitado del .ini archivo. |



 

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

 

 




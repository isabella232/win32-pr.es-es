---
description: La acción WriteIniValues escribe la información .ini archivo que la aplicación necesita escribir en sus .ini archivos.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: WriteIniValues (Acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2551725e7b12a697e35b08b403011044bbd631b3ff5bf3d0a5923ecb4c99e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942103"
---
# <a name="writeinivalues-action"></a>WriteIniValues (Acción)

La acción WriteIniValues escribe la información .ini archivo que la aplicación necesita escribir en sus .ini archivos. La escritura de esta información se encuentra en la tabla [Component](component-table.md). Se escribe .ini valor si el componente correspondiente se ha establecido para instalarse localmente o ejecutarse desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallValidate debe ir antes de la acción WriteIniValues. Si hay una [acción RemoveIniValues en](removeinivalues-action.md) la secuencia, debe ir antes de la acción WriteIniValues.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción              |
|-------|-----------------------------------------|
| \[1\] | Identificador de .ini archivo.                |
| \[2\] | .ini clave de archivo en la sección siguiente. |
| \[3\] | Elemento quitado de .ini archivo.            |
| \[4\] | Valor quitado del .ini archivo.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla IniFile](inifile-table.md)
</dt> </dl>

 

 




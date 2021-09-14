---
description: La acción WriteIniValues escribe la información .ini archivo que la aplicación necesita escribir en sus .ini archivos.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: WriteIniValues (acción)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071802"
---
# <a name="writeinivalues-action"></a>WriteIniValues (acción)

La acción WriteIniValues escribe la información .ini archivo que la aplicación necesita escribir en sus .ini archivos. La escritura de esta información se encuentra en la tabla [Component](component-table.md). Se .ini valor si el componente correspondiente se ha establecido para instalarse localmente o ejecutarse desde el origen.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallValidate debe ir antes de la acción WriteIniValues. Si hay una [acción RemoveIniValues en](removeinivalues-action.md) la secuencia, debe ir antes de la acción WriteIniValues.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción              |
|-------|-----------------------------------------|
| \[1\] | Identificador de .ini archivo.                |
| \[2\] | .ini clave de archivo en la sección siguiente. |
| \[3\] | Elemento quitado del .ini archivo.            |
| \[4\] | Valor quitado de .ini archivo.           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla IniFile](inifile-table.md)
</dt> </dl>

 

 




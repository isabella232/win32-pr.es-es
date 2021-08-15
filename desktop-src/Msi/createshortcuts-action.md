---
description: La acción CreateShortcuts administra la creación de accesos directos.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Acción CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209dbd38d64abb2ddedb267512dd3872991d58071769d25606ed364a15c6d958
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649745"
---
# <a name="createshortcuts-action"></a>Acción CreateShortcuts

La acción CreateShortcuts administra la creación de accesos directos.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CreateShortcuts debe ir después de [la acción InstallFiles](installfiles-action.md) y [la acción RemoveShortcuts.](removeshortcuts-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | Identificador del acceso directo creado. |



 

## <a name="remarks"></a>Comentarios

La acción CreateShortcuts crea accesos directos a los archivos clave de los componentes de las características que se seleccionan para la instalación o el anuncio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de métodos abreviados](shortcut-table.md)
</dt> <dt>

[Tabla MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 




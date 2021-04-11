---
description: La acción CreateShortcuts administra la creación de accesos directos.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Acción CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083232"
---
# <a name="createshortcuts-action"></a>Acción CreateShortcuts

La acción CreateShortcuts administra la creación de accesos directos.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CreateShortcuts debe aparecer después de la acción [InstallFiles](installfiles-action.md) y la acción [RemoveShortcuts](removeshortcuts-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | Identificador del acceso directo creado. |



 

## <a name="remarks"></a>Observaciones

La acción CreateShortcuts crea accesos directos a los archivos de clave de los componentes de las características que se seleccionan para la instalación o el anuncio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de acceso directo](shortcut-table.md)
</dt> <dt>

[Tabla MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 




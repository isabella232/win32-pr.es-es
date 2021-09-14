---
description: La acción CreateShortcuts administra la creación de accesos directos.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Acción CreateShortcuts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158741"
---
# <a name="createshortcuts-action"></a>Acción CreateShortcuts

La acción CreateShortcuts administra la creación de accesos directos.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CreateShortcuts debe ir después de la acción [InstallFiles](installfiles-action.md) y [la acción RemoveShortcuts.](removeshortcuts-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | Identificador del acceso directo creado. |



 

## <a name="remarks"></a>Observaciones

La acción CreateShortcuts crea accesos directos a los archivos clave de componentes de características que se seleccionan para la instalación o el anuncio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de métodos abreviados](shortcut-table.md)
</dt> <dt>

[Tabla MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 




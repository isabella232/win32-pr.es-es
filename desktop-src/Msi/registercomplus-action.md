---
description: La acción RegisterComPlus registra las aplicaciones COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Acción RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156464"
---
# <a name="registercomplus-action"></a>Acción RegisterComPlus

La acción RegisterComPlus registra las aplicaciones COM+.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterComPlus debe seguir la acción [InstallFiles](installfiles-action.md) y la [acción UnregisterComPlus](unregistercomplus-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción              |
|-------|-----------------------------------------|
| \[1\] | IDENTIFICADOR de la aplicación COM+. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de ComPlus](complus-table.md)
</dt> <dt>

[Acción UnregisterComPlus](unregistercomplus-action.md)
</dt> <dt>

[Instalación de una aplicación COM+ con el Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




---
description: La acción UnregisterComPlus quita las aplicaciones COM+ del registro.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Acción UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499855"
---
# <a name="unregistercomplus-action"></a>Acción UnregisterComPlus

La acción UnregisterComPlus quita las aplicaciones COM+ del registro.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La [acción RegisterComPlus debe](registercomplus-action.md) seguir la acción [InstallFiles](installfiles-action.md) y la acción UnregisterComPlus.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Identificador de aplicación de la aplicación COM+ que se va a quitar. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acción RegisterComPlus](registercomplus-action.md)
</dt> <dt>

[Tabla Complus](complus-table.md)
</dt> <dt>

[Instalación de una aplicación COM+ con Windows Instalador](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




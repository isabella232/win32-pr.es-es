---
description: La acción UnregisterComPlus quita las aplicaciones COM+ del registro.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Acción UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171582"
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

[Instalación de una aplicación COM+ con Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 




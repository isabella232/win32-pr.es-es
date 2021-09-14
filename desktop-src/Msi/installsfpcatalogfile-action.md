---
description: La acción InstallSFPCatalogFile instala los catálogos usados por Windows Me para Windows File Protection.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Acción InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072034"
---
# <a name="installsfpcatalogfile-action"></a>Acción InstallSFPCatalogFile

La acción InstallSFPCatalogFile instala los catálogos usados por Windows Me para Windows File Protection. InstallSFPCatalogFile consulta las tablas [Component](component-table.md), [File ,](file-table.md) [FileSFPCatalog y](filesfpcatalog-table.md) [SFPCatalog](sfpcatalog-table.md). Los catálogos se instalan si están asociados a un archivo de un componente establecido para la instalación local o si están asociados a un archivo que se está reparando en un componente instalado localmente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallSFPCatalogFile debe secuenciarse antes [de InstallFiles](installfiles-action.md) y después [de CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nombre del catálogo que se va a instalar.                          |
| \[2\] | Nombre del catálogo del que depende la instalación de este catálogo. |



 

## <a name="remarks"></a>Observaciones

Catálogo que depende de otro catálogo instalado después del catálogo primario.

 

 




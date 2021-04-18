---
description: La acción InstallSFPCatalogFile instala los catálogos que usa Windows me para la protección de archivos de Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Acción InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686573"
---
# <a name="installsfpcatalogfile-action"></a>Acción InstallSFPCatalogFile

La acción InstallSFPCatalogFile instala los catálogos que usa Windows me para la protección de archivos de Windows. InstallSFPCatalogFile consulta la tabla de [componentes](component-table.md), la [tabla de archivos](file-table.md), la tabla [FileSFPCatalog](filesfpcatalog-table.md) y la tabla [SFPCatalog](sfpcatalog-table.md). Los catálogos se instalan si están asociados a un archivo en un componente que se establece para la instalación local o si están asociados a un archivo que se va a reparar en un componente instalado localmente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallSFPCatalogFile se debe secuenciar antes de [InstallFiles](installfiles-action.md) y después de [CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nombre del catálogo que se va a instalar.                          |
| \[2\] | Nombre del catálogo del que depende esta instalación de este catálogo. |



 

## <a name="remarks"></a>Observaciones

Catálogo que depende de otro Catálogo instalado después del catálogo primario.

 

 




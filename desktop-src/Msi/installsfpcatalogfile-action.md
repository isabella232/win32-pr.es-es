---
description: La acción InstallSFPCatalogFile instala los catálogos usados por Windows Me para Windows File Protection.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Acción InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f3992a64e5e3150759fdbc2c8221e6bd8672a2c75e72343280fb3e552f3cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787015"
---
# <a name="installsfpcatalogfile-action"></a>Acción InstallSFPCatalogFile

La acción InstallSFPCatalogFile instala los catálogos usados por Windows Me para Windows File Protection. InstallSFPCatalogFile consulta la tabla [Component](component-table.md), [la tabla File](file-table.md), la tabla [FileSFPCatalog](filesfpcatalog-table.md) y [la tabla SFPCatalog](sfpcatalog-table.md). Los catálogos se instalan si están asociados a un archivo de un componente que está establecido para la instalación local o si están asociados a un archivo que se está reparando en un componente instalado localmente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción InstallSFPCatalogFile debe secuenciarse antes [de InstallFiles](installfiles-action.md) y después [de CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Nombre del catálogo que se va a instalar.                          |
| \[2\] | Nombre del catálogo del que depende la instalación de este catálogo. |



 

## <a name="remarks"></a>Comentarios

Catálogo que depende de otro catálogo instalado después del catálogo primario.

 

 




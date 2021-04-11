---
description: La acción AppSearch usa firmas de archivo para buscar versiones existentes de los productos.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Acción AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276524"
---
# <a name="appsearch-action"></a>Acción AppSearch

La acción AppSearch usa firmas de archivo para buscar versiones existentes de los productos. La acción AppSearch puede usar esta información para determinar dónde se instalarán las actualizaciones. La acción AppSearch también se puede usar para establecer una propiedad en el valor existente de una entrada del archivo Registry o. ini.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

AppSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que la acción AppSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ejecutó en la secuencia InstallUISequence.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | Propiedad que contiene la ubicación del archivo. |
| \[2\] | Firma de archivo.                 |



 

## <a name="remarks"></a>Observaciones

La acción AppSearch requiere que la tabla de [firma](signature-table.md) esté presente en el paquete de instalación. Las firmas de archivo se muestran en la tabla de firmas. Una firma que no está en la tabla de signatura denota un directorio y la acción establece la propiedad en la ruta de acceso del directorio para esa firma.

La acción AppSearch busca firmas de archivo mediante la tabla [CompLocator](complocator-table.md) en primer lugar, la tabla [RegLocator](reglocator-table.md) siguiente, la tabla [IniLocator](inilocator-table.md) y, por último, la tabla [DrLocator](drlocator-table.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[AppSearch](appsearch-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 




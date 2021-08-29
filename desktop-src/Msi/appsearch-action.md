---
description: La acción AppSearch usa firmas de archivo para buscar versiones existentes de productos.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Acción de AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbd6a99bdca37074f8bade1b40aa4665895b26b3fee46fa9bc5e0b63632c4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066285"
---
# <a name="appsearch-action"></a>Acción de AppSearch

La acción AppSearch usa firmas de archivo para buscar versiones existentes de productos. La acción AppSearch puede usar esta información para determinar dónde se van a instalar las actualizaciones. La acción AppSearch también se puede usar para establecer una propiedad en el valor existente de un registro o .ini entrada de archivo.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

AppSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y [en la tabla InstallExecuteSequence](installexecutesequence-table.md). El instalador impide que la acción de AppSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ha ejecutado en la secuencia InstallUISequence.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | Propiedad que mantiene la ubicación del archivo. |
| \[2\] | Firma de archivo.                 |



 

## <a name="remarks"></a>Comentarios

La acción AppSearch requiere que la [tabla Signature](signature-table.md) esté presente en el paquete de instalación. Las firmas de archivo se muestran en la tabla Firma. Una firma que no está en la tabla Firma denota un directorio y la acción establece la propiedad en la ruta de acceso del directorio para esa firma.

La acción AppSearch busca firmas de archivo mediante la tabla [CompLocator](complocator-table.md) en primer lugar, la tabla [RegLocator](reglocator-table.md) siguiente, después la [tabla IniLocator](inilocator-table.md) y, por último, la [tabla DrLocator.](drlocator-table.md)

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

 

 




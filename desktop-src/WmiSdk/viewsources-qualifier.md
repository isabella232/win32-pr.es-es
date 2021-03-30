---
description: Todas las clases de vista deben tener un calificador de matriz de cadenas denominado ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Calificador ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815371"
---
# <a name="viewsources-qualifier"></a>Calificador ViewSources

Todas las clases de vista deben tener un calificador de matriz de cadenas denominado **ViewSources**. El calificador **ViewSources** contiene las consultas de origen que definen las instancias de origen usadas en la clase de vista. El valor del calificador **ViewSources** es una matriz de cadenas que contiene consultas [*lenguaje de consulta de WMI (WQL)*](gloss-w.md) . Puede definir clases de origen y restringir las instancias de origen que utiliza la clase de vista con la cláusula de [consulta con WQL](querying-with-wql.md)[Where](where-clause.md) para crear una vista filtrada.

El [proveedor de vistas](view-provider.md) hace coincidir las consultas de origen del calificador **ViewSources** con los espacios de nombres enumerados en el [calificador ViewSpaces](viewspaces-qualifier.md) en el orden en que se muestran las consultas y los espacios de nombres. El número de consultas de origen debe coincidir con el número de espacios de nombres enumerados en el calificador ViewSpaces. El orden en que se enumeran las consultas de origen determina los espacios de nombres desde los que se dibujan las instancias de origen.

En el ejemplo siguiente se seleccionan solo las instancias de la clase **LocalDisk** en las que el valor de la propiedad **FILESYSTEM** es "NTFS" y las instancias de la clase **RemoteDisk** en las que el valor de la propiedad **FreeSpace** es mayor que 45 megabytes:


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> El número de consultas de origen que se pueden definir para las clases de vista de combinación depende del número de instancias devueltas por estas consultas y de cuántas formas se pueden combinar con estas instancias. El número de combinaciones posibles de instancias de origen para las clases de vista crece exponencialmente, por lo que las consultas de código fuente para las clases de vista de combinación son lo más sencillas posible.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 





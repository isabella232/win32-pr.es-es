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
ms.openlocfilehash: b2a0cadf3e1469fbdaf347b269813e76b780348d28482a00b4de290aaf4e0f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120765"
---
# <a name="viewsources-qualifier"></a>Calificador ViewSources

Todas las clases de vista deben tener un calificador de matriz de cadenas denominado **ViewSources.** El **calificador ViewSources** contiene las consultas de origen que definen las instancias de origen usadas en la clase de vista. El valor del **calificador ViewSources** es una matriz de cadenas [*que lenguaje de consulta de WMI consultas (WQL).*](gloss-w.md) Puede definir clases de origen y restringir las instancias de origen que usa la clase de vista con la cláusula[WHERE](where-clause.md) de Consulta con [WQL](querying-with-wql.md)para crear una vista filtrada.

El [proveedor de](view-provider.md) vistas coincide con las consultas de origen del calificador **ViewSources** con los espacios de nombres enumerados en el calificador [ViewSpaces](viewspaces-qualifier.md) en el orden en que se enumeran las consultas y los espacios de nombres. El número de consultas de origen debe coincidir con el número de espacios de nombres enumerados en el calificador ViewSpaces. El orden en el que se enumeran las consultas de origen determina los espacios de nombres a partir de los cuales se dibujan las instancias de origen.

En el ejemplo siguiente solo se seleccionan las instancias de la clase **LocalDisk** donde el valor de la propiedad **FileSystem** es "NTFS" y las instancias de la clase **RemoteDisk** donde el valor de la propiedad **FreeSpace** es superior a 45 megabytes:


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
> El número de consultas de origen que puede definir para las clases de vista de combinación depende del número de instancias que devuelven estas consultas y del número de maneras en que se pueden unir estas instancias. El número de combinaciones posibles de instancias de origen para las clases de vista crece exponencialmente, por lo que las consultas de origen de las clases de vista de combinación son lo más sencillas posible.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 





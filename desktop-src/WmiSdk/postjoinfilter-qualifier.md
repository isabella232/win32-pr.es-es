---
description: Puede filtrar las instancias de una clase de vista de combinación asignando una consulta WQL al calificador PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Calificador PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706753"
---
# <a name="postjoinfilter-qualifier"></a>Calificador PostJoinFilter

Puede filtrar las instancias de una clase de vista de combinación asignando una consulta WQL al calificador **PostJoinFilter** . El valor de la consulta WQL se aplica a las instancias de la clase de vista join. Puede utilizar este calificador para restringir las instancias de la clase de vista a aquellas que cumplan condiciones específicas. La consulta WQL siguiente filtra las instancias de una clase de combinación llamadas basadas en instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Existen varias restricciones en el uso de este calificador:

-   **PostJoinFilter** solo está disponible para las clases de vista de combinación.
-   El nombre de clase y los nombres de propiedad especificados en la consulta hacen referencia a las propiedades de la clase de vista, no a la clase de origen.
-   No se permite la exclusión de propiedades; solo `SELECT *` se permiten consultas de tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 


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
ms.openlocfilehash: be491c0bfefe77c2bf016789786212047d5ca8d00570c84057b8e8e346fb382e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317029"
---
# <a name="postjoinfilter-qualifier"></a>Calificador PostJoinFilter

Puede filtrar las instancias de una clase de vista de combinación asignando una consulta WQL al **calificador PostJoinFilter.** El valor de la consulta WQL se aplica a las instancias de la clase de vista de combinación. Puede usar este calificador para restringir las instancias de la clase de vista a las que cumplen condiciones específicas. La siguiente consulta WQL filtra las instancias de una clase de combinación llamada en función de las instancias de [**\_ LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Hay varias restricciones para el uso de este calificador:

-   **PostJoinFilter** solo está disponible para unir clases de vista.
-   El nombre de clase y los nombres de propiedad especificados en la consulta hacen referencia a las propiedades de la clase de vista, no a la clase de origen.
-   No se permite la exclusión de propiedades; solo `SELECT *` se permiten consultas de tipo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Calificadores específicos del proveedor de vistas**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 


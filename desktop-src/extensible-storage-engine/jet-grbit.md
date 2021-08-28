---
description: 'Más información sobre: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92fa6dffd94d2a1790811881fcdba86665ebb880
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482251"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_grbit"></a>JET_GRBIT

El **JET_GRBIT** de datos es un grupo de bits que contienen constantes que son específicas de las funciones y estructuras en las que se usa.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipo de datos

JET_GRBIT

En general, las constantes que se usan como valores para este tipo de datos reflejan el nombre del elemento de API en el que se usan. Por ejemplo, todas las constantes que se pasan [a JetRetrieveColumn](./jetretrievecolumn-function.md) comienzan por "JET_bitRetrieve". De forma similar, todas las constantes que se pasan [a JetSetColumn](./jetsetcolumn-function.md) comienzan por "JET_bitSet".

Un valor de cero hace que se ignore el parámetro.

### <a name="remarks"></a>Comentarios

Para obtener más información, vea la función o estructura específica. Las opciones normalmente se pasan como un conjunto de marcas que se pueden combinar.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)

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
ms.openlocfilehash: 7aa3a0331244aa1f5dd07794204d5a94d57aeadb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070235"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Se aplica a:** Windows | Windows Servidor_

## <a name="jet_grbit"></a>JET_GRBIT

El **JET_GRBIT** tipo de datos es un grupo de bits que contienen constantes que son específicas de las funciones y estructuras en las que se usa.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Tipo de datos

JET_GRBIT

En general, las constantes que se usan como valores para este tipo de datos reflejan el nombre del elemento de API en el que se usan. Por ejemplo, todas las constantes que se pasan [a JetRetrieveColumn](./jetretrievecolumn-function.md) comienzan por "JET_bitRetrieve". De forma similar, todas las constantes que se pasan [a JetSetColumn](./jetsetcolumn-function.md) comienzan por "JET_bitSet".

Un valor de cero hace que se ignore el parámetro.

### <a name="remarks"></a>Observaciones

Para obtener más información, vea la función o estructura específica. Las opciones normalmente se pasan como un conjunto de marcas que se pueden combinar.

### <a name="requirements"></a>Requisitos


| Requisito | Value |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)

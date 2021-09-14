---
description: El tipo de datos LARGEINT define un valor \_ LARGE INTEGER.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon.h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171417"
---
# <a name="largeint"></a>LARGEINT

El **tipo de datos LARGEINT** define un valor LARGE [**\_ INTEGER.**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Observaciones

El **miembro lpLargeIntTable** de la [**estructura SET**](set.md) apunta a una matriz de estructuras **SET** que definen uno o varios valores LARGEINT. Cuando se especifica este tipo de estructura **SET,** Monitor de red muestra una de las etiquetas siguientes con cada valor LARGEINT que encuentra en el paquete de protocolo.

-   Coincide con el valor establecido. El valor LARGEINT se incluye en el conjunto.
-   Valor establecido desconocido. El valor LARGEINT no se incluye en el conjunto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 


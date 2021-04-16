---
description: El tipo de LARGEINT define un \_ valor entero grande.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677017"
---
# <a name="largeint"></a>LARGEINT

El tipo de **LARGEINT** define un [**valor \_ entero grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Observaciones

El miembro **lpLargeIntTable** de la estructura de [**conjunto**](set.md) apunta a una matriz de estructuras **set** que definen uno o más valores de LARGEINT. Cuando se especifica este tipo de estructura de **conjunto** , monitor de red muestra una de las siguientes etiquetas con cada valor de LARGEINT que encuentra en el paquete del protocolo.

-   Coincide con el valor establecido. El valor LARGEINT se incluye en el conjunto.
-   Valor establecido desconocido. El valor LARGEINT no se incluye en el conjunto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 


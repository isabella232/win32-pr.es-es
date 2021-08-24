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
ms.openlocfilehash: a6eedf739d9d0b4285d0198ae905672dbbb7848a2b7d9ba106abb6a59fcdc4d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742655"
---
# <a name="largeint"></a>LARGEINT

El **tipo de datos LARGEINT** define un valor LARGE [**\_ INTEGER.**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Comentarios

El **miembro lpLargeIntTable** de la estructura [**SET**](set.md) apunta a una matriz de estructuras **SET** que definen uno o varios valores LARGEINT. Cuando se especifica este tipo de estructura **SET,** Monitor de red muestra una de las siguientes etiquetas con cada valor LARGEINT que encuentra en el paquete de protocolo.

-   Coincide con el valor establecido. El valor LARGEINT se incluye en el conjunto.
-   Valor de conjunto desconocido. El valor LARGEINT no se incluye en el conjunto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[SET](set.md)
</dt> </dl>

 


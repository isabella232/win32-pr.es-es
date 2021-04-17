---
description: Tenga en cuenta que esta API está en desuso. Las nuevas aplicaciones no deben utilizarla. El tipo de datos MSPID identifica el propósito de una secuencia de medios.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (Mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690736"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> Esta API está en desuso. Las nuevas aplicaciones no deben utilizarla.

 

El tipo de datos **MSPID** identifica el propósito de una secuencia de medios.


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>Observaciones

**MSPID** es simplemente una definición de tipo para GUID. Se definen los siguientes MSPIDs.



| Value               | Descripción           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | Secuencia de vídeo principal. |
| MSPID \_ PrimaryAudio | Secuencia de audio principal. |



 

El tipo **REFMSPID** define una referencia a un **MSPID**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mmstream. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos de transmisión por secuencias multimedia](multimedia-streaming-data-types.md)
</dt> </dl>

 

 





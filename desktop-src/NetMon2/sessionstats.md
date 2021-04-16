---
description: La estructura SESSIONSTATS proporciona estadísticas sobre una sesión.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Estructura SESSIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276275"
---
# <a name="sessionstats-structure"></a>Estructura SESSIONSTATS

La estructura **SESSIONSTATS** proporciona estadísticas sobre una [*sesión*](s.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**NextSession**
</dt> <dd>

Índice de la siguiente sesión del propietario de la estación.

</dd> <dt>

**StationOwner**
</dt> <dd>

Índice de una estación propietaria dentro de la matriz de estructura [STATIONSTATS](stationstats.md) asociada. La estación propietaria es la estación que inició la sesión, la estación que envió los paquetes de la sesión.

</dd> <dt>

**StationPartner**
</dt> <dd>

Índice de la otra estación dentro de la matriz de estructura [STATIONSTATS](stationstats.md) asociada. La estación de asociado es la estación que recibió los paquetes de la sesión.

</dd> <dt>

**Marcas**
</dt> <dd>

Este miembro está obsoleto.

</dd> <dt>

**TotalPacketsSent**
</dt> <dd>

Número de paquetes enviados en la sesión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Monitor de red almacena información de la sesión y de la estación en dos matrices asociadas, cuyos elementos son **SESSIONSTATS** y [STATIONSTATS](stationstats.md) , respectivamente. Los miembros de estas estructuras se pueden usar para navegar entre ellos. Por ejemplo, para pasar a la siguiente sesión de un propietario de una estación concreta, use **NextSession**. Para saltar al propietario y a la estación de socio comercial de la sesión en la matriz STATIONSTATS, use el índice proporcionado en **StationOwner** y **StationPartner**.

> [!Note]  
> La matriz SESSIONSTATS contiene un elemento para cada sesión en la captura actual. El algoritmo Monitor de red usa para agregar elementos a la matriz SESSIONSTATS se basa en la grabación eficaz de la información mientras la captura está en curso. Por consiguiente, la siguiente sesión de una estación propietaria específica no es siempre el siguiente elemento de la matriz.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IStas:: GetConversationStatistics](istats-getconversationstatistics.md)
</dt> </dl>

 

 





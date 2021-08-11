---
title: MPTHREAT_TYPE enumeración (MpClient.h)
description: Posibles tipos de amenazas.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE enumeración de características heredadas Windows entorno
- PMPTHREAT_TYPE puntero de enumeración Heredados Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858501603b67451db9b565609d0c263040d2186cf44d91646e6df6ce3871ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247146"
---
# <a name="mpthreat_type-enumeration"></a>Enumeración MPTHREAT \_ TYPE

Posibles tipos de amenazas.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**TIPO MPTHREAT \_ \_ KNOWNBAD**
</dt> <dd>

Se detectó una amenaza no válida conocida a través de la firma.

</dd> <dt>

<span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**COMPORTAMIENTO DEL TIPO \_ \_ MPTHREAT**
</dt> <dd>

Se detectó una amenaza sospechosa a través de la supervisión del comportamiento.

</dd> <dt>

<span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**TIPO MPTHREAT \_ \_ DESCONOCIDO**
</dt> <dd>

Amenazas desconocidas (sin clasificar).

</dd> <dt>

<span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**TIPO MPTHREAT \_ \_ KNOWNGOOD**
</dt> <dd>

Amenaza buena conocida.

</dd> <dt>

<span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ TYPE \_ NIS**
</dt> <dd>

Detección de amenazas de NIS.

</dd> <dt>

<span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT \_ TYPE \_ MAXVALUE**
</dt> <dd>

Valor máximo posible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






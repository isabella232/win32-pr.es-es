---
title: MPCOMPONENT_VERSION estructura (MpClient. h)
description: Versión y tiempo de actualización de un componente individual.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCOMPONENT_VERSION características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996338"
---
# <a name="mpcomponent_version-structure"></a>Estructura de la versión de MPCOMPONENT \_

Versión y tiempo de actualización de un componente individual.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Versión**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Campo de versión. Cada **palabra** representa una versión principal, secundaria, de compilación y de revisión.

</dd> <dt>

**UpdateTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Hora de la última actualización del componente, en formato **FILETIME** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 






---
title: MPSCAN_TYPE enumeración (MpClient.h)
description: Tipo de examen realizado.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE enumeración heredada de Windows environment
- PMPSCAN_TYPE puntero de enumeración heredados Windows environment
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56906bfc9ad57f93bac4c8b8c27360b5ade9592ac33efe39574fe8890299e13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747136"
---
# <a name="mpscan_type-enumeration"></a>Enumeración \_ MPSCAN TYPE

Tipo de examen realizado.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**TIPO MPSCAN \_ \_ DESCONOCIDO**
</dt> <dd>

Exclusivamente para uso interno.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**TIPO DE MPSCAN \_ \_ RÁPIDO**
</dt> <dd>

Examina los procesos en ejecución y varios puntos ASEP en el sistema donde normalmente se oculta el malware.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**TIPO DE MPSCAN \_ \_ COMPLETO**
</dt> <dd>

Realiza un examen rápido seguido de un examen de todas las unidades fijas del sistema.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**RECURSO DE \_ TIPO MPSCAN \_**
</dt> <dd>

Examina recursos específicos, como archivos o carpetas.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN \_ TYPE \_ MAXVALUE**
</dt> <dd>

Valor máximo posible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 






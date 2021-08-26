---
description: Representa el tipo de información de la estructura SYSTEM \_ CPU \_ SET \_ INFORMATION.
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: CPU_SET_INFORMATION_TYPE enumeración (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 7c932a143553c1101d6a81bac86ba54e21603eaf80ed5d2613484bff22a7e625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101935"
---
# <a name="cpu_set_information_type-enumeration"></a>Enumeración \_ SET \_ INFORMATION TYPE \_ de CPU

Representa el tipo de información de la estructura [**SYSTEM \_ CPU SET \_ \_ INFORMATION.**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

## <a name="syntax"></a>Syntax


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**
</dt> <dd>

La estructura contiene información del conjunto de CPU.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                       |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                              |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h (incluir Windows.h)</dt> </dl> |



 

 





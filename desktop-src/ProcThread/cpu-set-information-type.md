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
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161058"
---
# <a name="cpu_set_information_type-enumeration"></a>Enumeración \_ SET \_ INFORMATION TYPE \_ de CPU

Representa el tipo de información de la estructura [**SYSTEM \_ CPU SET \_ \_ INFORMATION.**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)

## <a name="syntax"></a>Sintaxis


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
| Encabezado<br/>                   | <dl> <dt>Processthreadsapi.h (incluir Windows.h)</dt> </dl> |



 

 





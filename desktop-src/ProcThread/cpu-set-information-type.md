---
description: Representa el tipo de información de la estructura de información de conjunto de CPU del sistema \_ \_ \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Enumeración CPU_SET_INFORMATION_TYPE (Processthreadapi. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677867"
---
# <a name="cpu_set_information_type-enumeration"></a>\_ \_ Enumeración de tipo de información de conjunto de CPU \_

Representa el tipo de información de la estructura de [**\_ información de \_ conjunto \_ de CPU del sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .

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

La estructura contiene información de conjunto de CPU.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Processthreadsapi. h (incluir Windows. h)</dt> </dl> |



 

 





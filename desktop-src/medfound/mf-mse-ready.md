---
description: Define los diferentes Estados preparados de la extensión de origen multimedia.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Enumeración MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910202"
---
# <a name="mf_mse_ready-enumeration"></a>\_ \_ Enumeración preparada para MSE de MF

Define los diferentes Estados preparados de la extensión de origen multimedia.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ preparado \_ cerrado**
</dt> <dd>

El origen del medio está cerrado.

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE \_ listo \_ abierto**
</dt> <dd>

El origen del medio está abierto.

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF \_ MSE \_ preparado \_ terminado**
</dt> <dd>

El origen de los medios ha finalizado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 





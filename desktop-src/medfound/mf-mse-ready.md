---
description: Define los distintos estados listos de la extensión de origen de medios.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: MF_MSE_READY enumeración
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
ms.openlocfilehash: 28f476c32abbffa8faadd8a7c527f07d81632eee10f1c6cfc54eacc926b4f4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104581"
---
# <a name="mf_mse_ready-enumeration"></a>Enumeración \_ MF MSE \_ READY

Define los distintos estados listos de la extensión de origen de medios.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ READY \_ CLOSED**
</dt> <dd>

El origen de medios está cerrado.

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE \_ READY \_ OPEN**
</dt> <dd>

El origen multimedia está abierto.

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF \_ MSE \_ READY \_ ENDED**
</dt> <dd>

El origen del medio ha finalizado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation enumeraciones](media-foundation-enumerations.md)
</dt> </dl>

 

 





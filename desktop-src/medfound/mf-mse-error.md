---
description: Define los distintos estados de error de la extensión de origen de medios.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: MF_MSE_ERROR enumeración
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 71246aaa2897540b272360a790718f8d5900934108c98dfcc6b4023898f9f2db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104591"
---
# <a name="mf_mse_error-enumeration"></a>MF \_ MSE \_ ERROR (enumeración)

Define los distintos estados de error de la extensión de origen de medios.

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF \_ MSE \_ ERROR \_ NOERROR**
</dt> <dd>

No especifica ningún error.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**MF \_ MSE \_ ERROR \_ NETWORK**
</dt> <dd>

Especifica un error con la red.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**DESCODIFICACIÓN \_ DE \_ ERRORES DE MF MSE \_**
</dt> <dd>

Especifica un error con lacoding.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**\_ERROR DESCONOCIDO DE MF MSE \_ \_ \_**
</dt> <dd>

Especifica un error desconocido.

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

 

 





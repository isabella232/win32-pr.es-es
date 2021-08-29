---
description: Indica que se está iniciando el proceso de suspensión y que los recursos se deben poner en un estado coherente.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: MÉTODO IMFCdmSuspendNotify::Begin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 1665102e336901d634d2ea948ad338842ef3a6d04bf4b7f43ba5297f1df13198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724567"
---
# <a name="imfcdmsuspendnotifybegin-method"></a>MÉTODO IMFCdmSuspendNotify::Begin

Indica que se está iniciando el proceso de suspensión y que los recursos se deben poner en un estado coherente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFCdmSuspendNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 





---
description: Se usa para indicar que se ha producido un error con el búfer de origen.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: MÉTODO IMFSourceBufferNotify::OnError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 0602340011bae5af974a3441b42d62d392394b79854015acc68da0b1c2fcf538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957814"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>MÉTODO IMFSourceBufferNotify::OnError

Se usa para indicar que se ha producido un error con el búfer de origen.

## <a name="syntax"></a>Sintaxis


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hr* \[ En\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 





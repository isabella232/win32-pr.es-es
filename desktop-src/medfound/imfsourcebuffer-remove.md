---
description: Quita los segmentos multimedia definidos por el intervalo de tiempo especificado de IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: MÉTODO IMFSourceBuffer::Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: af9aed011a1a4b53733d70646fc14b21e7c97f9d193a60e679f5f5f532679e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941915"
---
# <a name="imfsourcebufferremove-method"></a>MÉTODO IMFSourceBuffer::Remove

Quita los segmentos de medios definidos por el intervalo de tiempo especificado del [**elemento IMFSourceBuffer.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*start* \[ En\]
</dt> <dd>

Inicio del intervalo de tiempo.

</dd> <dt>

*end* \[ En\]
</dt> <dd>

Final del intervalo de tiempo.

</dd> </dl>

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

[**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 





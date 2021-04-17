---
description: Establece la duración del origen del medio en unidades de 100-nanosegundos.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'IMFMediaSourceExtension:: SetDuration (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697957"
---
# <a name="imfmediasourceextensionsetduration-method"></a>IMFMediaSourceExtension:: SetDuration (método)

Establece la duración del origen del medio en unidades de 100-nanosegundos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*duración* \[ de de\]
</dt> <dd>

La duración del origen del medio en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





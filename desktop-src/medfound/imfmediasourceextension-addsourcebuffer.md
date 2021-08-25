---
description: Agrega un ELEMENTO IMFSourceBuffer a la colección de búferes asociados a LAEXTENSIONMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: MÉTODO IMFMediaSourceExtension::AddSourceBuffer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: b49a7c4fb0cb9e45ab0c2823d92ceb6e4076dfcaef4d2e8450f1f3d07f474279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942035"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a>MÉTODO IMFMediaSourceExtension::AddSourceBuffer

Agrega [**un elemento IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) a la colección de búferes asociados a [**LA CLASE IMFMediaSourceExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd></dd> <dt>

*pNotify* \[ En\]
</dt> <dd></dd> <dt>

*ppSourceBuffer* \[ out\]
</dt> <dd></dd> </dl>

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

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





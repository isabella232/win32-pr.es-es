---
description: Quita el búfer de origen especificado de la colección de búferes de origen administrados por el objeto IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: MÉTODO IMFMediaSourceExtension::RemoveSourceBuffer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 52c15882b57191169f033ab8a3b6c2f50f10f8e20b8f081c7bc70b7509b9a58b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013975"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>MÉTODO IMFMediaSourceExtension::RemoveSourceBuffer

Quita el búfer de origen especificado de la colección de búferes de origen administrados por el [**objeto IMFMediaSourceExtension.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSourceBuffer* \[ En\]
</dt> <dd>

Búfer que se quitará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





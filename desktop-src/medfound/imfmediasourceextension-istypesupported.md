---
description: Obtiene un valor que indica si el origen multimedia admite el tipo MIME especificado.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: MÉTODO IMFMediaSourceExtension::IsTypeSupported
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: e2292ab717914e29a7741fed997b0f8b8b16e152e2fa889dd7ecb04bbb98aaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974344"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>MÉTODO IMFMediaSourceExtension::IsTypeSupported

Obtiene un valor que indica si el origen multimedia admite el tipo MIME especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Tipo de medio para el que se comprobará la compatibilidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si se admite el tipo de medio; de lo contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 





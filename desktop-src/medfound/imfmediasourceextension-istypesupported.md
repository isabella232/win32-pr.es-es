---
description: Obtiene un valor que indica si el origen de medios admite el tipo MIME especificado.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'IMFMediaSourceExtension:: IsTypeSupported (método)'
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
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697958"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>IMFMediaSourceExtension:: IsTypeSupported (método)

Obtiene un valor que indica si el origen de medios admite el tipo MIME especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* \[ de de\]
</dt> <dd>

Tipo de medio para el que se va a comprobar la compatibilidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**true** si se admite el tipo de medio; en caso contrario, **false**.

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

 

 





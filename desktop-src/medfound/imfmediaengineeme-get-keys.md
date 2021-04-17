---
description: Obtiene el objeto de claves multimedia asociado al motor multimedia o null si no hay un objeto de claves multimedia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'IMFMediaEngineEME:: get_Keys (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717390"
---
# <a name="imfmediaengineemeget_keys-method"></a>IMFMediaEngineEME:: get \_ Keys (método)

Obtiene el objeto de claves multimedia asociado al motor multimedia o **null** si no hay un objeto de claves multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mykeys* 
</dt> <dd>

Objeto de claves multimedia asociado al motor multimedia o **null** si no hay un objeto de claves multimedia.

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

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 





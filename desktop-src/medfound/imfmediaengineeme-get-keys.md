---
description: Obtiene el objeto de claves multimedia asociado al motor de medios o null si no hay un objeto de claves multimedia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: MÉTODO IMFMediaEngineEME::get_Keys
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
ms.openlocfilehash: 2df0be51eaf634879c2f8e90ae864b2e0dad5ce54271c55f5a81251141471843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942085"
---
# <a name="imfmediaengineemeget_keys-method"></a>MÉTODO IMFMediaEngineEME::get \_ Keys

Obtiene el objeto de claves multimedia asociado al motor de medios o **null** si no hay un objeto de claves multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Llaves* 
</dt> <dd>

Objeto de claves multimedia asociado al motor de medios o **null** si no hay un objeto de claves multimedia.

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

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 





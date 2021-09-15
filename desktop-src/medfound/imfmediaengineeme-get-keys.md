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
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579973"
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

*claves* 
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
| IDL<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 





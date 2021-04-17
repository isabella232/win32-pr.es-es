---
description: Obtiene todos los identificadores de propiedad disponibles en un perfil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'IScanProfile:: GetAllPropIDs (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696622"
---
# <a name="iscanprofilegetallpropids-method"></a>IScanProfile:: GetAllPropIDs (método)

Obtiene todos los identificadores de propiedad disponibles en un perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*número* \[ de in, out\]
</dt> <dd>

Tipo: **ULong \** _

Número de identificadores de propiedad solicitados o devueltos.

</dd> <dt>

_ppid * \[ out\]
</dt> <dd>

Tipo: **PROPID \** _

Puntero a una matriz de identificadores de propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 





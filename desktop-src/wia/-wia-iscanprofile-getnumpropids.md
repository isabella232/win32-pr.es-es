---
description: Obtiene el número de identificadores de propiedad de un perfil.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'IScanProfile:: GetNumPropIDS (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154876"
---
# <a name="iscanprofilegetnumpropids-method"></a>IScanProfile:: GetNumPropIDS (método)

Obtiene el número de identificadores de propiedad de un perfil.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*número* \[ de enuncia\]
</dt> <dd>

Tipo: **ULong \** _

El número de identificadores de propiedad en el perfil.

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

 

 





---
description: El método IsChildOf determina si una solicitud es un elemento secundario de una solicitud especificada (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess:: IsChildOf (método) (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277925"
---
# <a name="iwbemcausalityaccessischildof-method"></a>IWbemCausalityAccess:: IsChildOf (método)

El método **IsChildOf** determina si una solicitud es un elemento secundario de una solicitud especificada (pId). Una solicitud primaria puede tener varias solicitudes secundarias. Cada solicitud se identifica mediante un identificador único global (GUID) y puede tener una solicitud primaria o puede ser una solicitud Top. Un GUID es un número único de 128 bits.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pId* \[ de de\]
</dt> <dd>

Valor GUID que identifica de forma única una solicitud. Por ejemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve correcto si la solicitud especificada es un elemento secundario de la solicitud que llama al método **IsChildOf** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 





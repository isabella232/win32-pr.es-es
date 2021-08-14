---
description: El método IsChildOf determina si una solicitud es un elemento secundario de una solicitud especificada (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: Método IWbemCausalityAccess::IsChildOf (Wbemint.h)
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
ms.openlocfilehash: 509508d5e1a273dc681cf3c9f645ead1037408d6ecfe5ed666186ba6e2a2c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318297"
---
# <a name="iwbemcausalityaccessischildof-method"></a>IWbemCausalityAccess::IsChildOf (método)

El **método IsChildOf** determina si una solicitud es un elemento secundario de una solicitud especificada (pId). Una solicitud primaria puede tener varias solicitudes secundarias. Cada solicitud se identifica mediante un identificador único global (GUID) y puede tener una solicitud primaria o puede ser una solicitud principal. Un GUID es un número único de 128 bits.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pId* \[ En\]
</dt> <dd>

Valor GUID que identifica de forma única una solicitud. Por ejemplo, 5b2fc63a-8af4-44cb-960c-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve correctamente si la solicitud especificada es un elemento secundario de la solicitud que llama al **método IsChildOf.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemint.h</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 





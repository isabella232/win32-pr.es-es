---
title: Propiedad TargetName de ITsSbTarget
description: Especifica o recupera el nombre del destino.
ms.assetid: ba5c3158-b4bc-457f-94ea-adb2e0852129
ms.tgt_platform: multiple
keywords:
- Propiedad TargetName Servicios de Escritorio remoto
- Propiedad TargetName Servicios de Escritorio remoto , interfaz ITsSbTarget
- Interfaz ITsSbTarget Servicios de Escritorio remoto , propiedad TargetName
- Propiedad TargetName Servicios de Escritorio remoto , interfaz ITsSbTargetEx
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto , propiedad TargetName
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetName
- ITsSbTarget.get_TargetName
- ITsSbTarget.put_TargetName
- ITsSbTargetEx.TargetName
- ITsSbTargetEx.get_TargetName
- ITsSbTargetEx.put_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971ae66d162464c49d7eb4206f1fbddf206707c2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467872"
---
# <a name="itssbtargettargetname-property"></a>Propiedad ITsSbTarget::TargetName

Especifica o recupera el nombre del destino.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_TargetName(
  [in]          BSTR Val
);

HRESULT get_TargetName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **BSTR** que especifica el nombre de destino.

## <a name="remarks"></a>Comentarios

Esta propiedad era de solo lectura antes de Windows Server 2012.

## <a name="requirements"></a>Requisitos




| | | Cliente mínimo admitido<br /> | Ninguno admitido<br /> | | Servidor mínimo admitido<br /> | Windows Server 2012<br /> | | IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | | IID<br /> | IID_ITsSbTarget se define como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 en Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 






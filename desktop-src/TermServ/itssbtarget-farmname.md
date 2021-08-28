---
title: Propiedad FarmName de ITsSbTarget
description: Recupera o especifica el nombre de la granja a la que está unido este destino.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Propiedad FarmName Servicios de Escritorio remoto
- Propiedad FarmName Servicios de Escritorio remoto , interfaz ITsSbTarget
- Interfaz ITsSbTarget Servicios de Escritorio remoto , propiedad FarmName
- Propiedad FarmName Servicios de Escritorio remoto , interfaz ITsSbTargetEx
- Interfaz ITsSbTargetEx Servicios de Escritorio remoto , propiedad FarmName
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b1c36a1a44f38dac11a7e474d7fefb80a09948
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988298"
---
# <a name="itssbtargetfarmname-property"></a>Propiedad ITsSbTarget::FarmName

Recupera o especifica el nombre de la granja a la que está unido este destino.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **BSTR** que contiene el nombre de la granja.

## <a name="requirements"></a>Requisitos




| Requisito | Value |
|--------|-------|
| Cliente mínimo compatible<br /> | No se admite ninguno<br /> | 
| Servidor mínimo compatible<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget se define como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 en Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 






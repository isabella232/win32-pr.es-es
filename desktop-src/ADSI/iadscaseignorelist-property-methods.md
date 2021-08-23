---
title: Métodos de propiedad IADsCaseIgnoreList (Iads.h)
description: El método de propiedad de la interfaz IADsCaseIgnoreList establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsCaseIgnoreList ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e2f07d3c4afa6cd55f6a757ccae6f2d1076b954e0afdd0c82c8a5247af33f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961924"
---
# <a name="iadscaseignorelist-property-methods"></a>Métodos de propiedad IADsCaseIgnoreList

El método de propiedad [**de la interfaz IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**CaseIgnoreList**
</dt> <dd> <dl>

Secuencia ordenada de cadenas que no tienen en cuenta mayúsculas de minúsculas.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsCaseIgnoreList se define como 7B66B533-4680-11D1-A3B4-00C04FB950DC<br/>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[**ADS \_ CASEIGNORE \_ LIST**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 






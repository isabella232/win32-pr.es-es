---
title: Métodos de propiedad IADsPostalAddress (Iads.h)
description: El método de propiedad de la interfaz IADsPostalAddress establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd01887751a4389984a4bc765d924d6c8a8e81dd9a65be3b7a868a3cbb845cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691132"
---
# <a name="iadspostaladdress-property-methods"></a>Métodos de propiedad IADsPostalAddress

El método de propiedad de [**la interfaz IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**PostalAddress**
</dt> <dd> <dl>

Matriz de seis cadenas que contiene la dirección postal del usuario.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
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
| IID<br/>                      | IID \_ IADsPostalAddress se define como 7ADECF29-4680-11D1-A3B4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[**ADS \_ POSTALADDRESS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 






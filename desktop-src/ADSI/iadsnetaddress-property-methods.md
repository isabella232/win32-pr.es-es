---
title: Métodos de propiedad IADsNetAddress (Iads.h)
description: El método de propiedad de la interfaz IADsNetAddress establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- AdsI de métodos de propiedad IADsNetAddress
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b3a6d7076350df339df9c3657635af8aed9ca0ad0dd21638155ff074efca312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961914"
---
# <a name="iadsnetaddress-property-methods"></a>Métodos de propiedad IADsNetAddress

El método de propiedad de [**la interfaz IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Dirección**
</dt> <dd> <dl>

Una dirección de red.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

**AddressType**
</dt> <dd> <dl>

Tipo de protocolos de comunicación.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsNetAddress se define como \_ B21A50A9-4080-11D1-A3AC-00C04FB950DC<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[**ADS \_ NETADDRESS**](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 






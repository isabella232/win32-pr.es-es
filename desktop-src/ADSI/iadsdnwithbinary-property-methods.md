---
title: Métodos de propiedad IADsDNWithBinary (Iads.h)
description: El método de propiedad de la interfaz IADsDNWithBinary establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsDNWithBinary ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ab9fb355f2602d290c064f6636a13375ea92fdfbf0d6d47c1c6cf8d61e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023503"
---
# <a name="iadsdnwithbinary-property-methods"></a>Métodos de propiedad IADsDNWithBinary

El método de propiedad [**de la interfaz IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**BinaryValue**
</dt> <dd> <dl>

GUID de un objeto asociado a un DN.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

**DNString**
</dt> <dd> <dl>

Cadena DN asociada al GUID de un objeto .

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
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
| IID<br/>                      | IID \_ IADsDNWithBinary se define como 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[**ADS \_ DN \_ CON \_ BINARY**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 






---
title: Métodos de propiedad IADsFaxNumber (Iads.h)
description: El método de propiedad de la interfaz IADsFaxNumber establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: f4d46b9d-8db2-47b3-b489-9ffc363e6ac6
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsFaxNumber ADSI
topic_type:
- apiref
api_name:
- IADsFaxNumber Property Methods
- IADsFaxNumber.TelephoneNumber
- IADsFaxNumber.get_TelephoneNumber
- IADsFaxNumber.put_TelephoneNumber
- IADsFaxNumber.Parameters
- IADsFaxNumber.get_Parameters
- IADsFaxNumber.put_Parameters
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1a740488c8f50dd90a0886b48b1c72f0e8e4560e50a741e8283b5a8ceb2360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082459"
---
# <a name="iadsfaxnumber-property-methods"></a>Métodos de propiedad IADsFaxNumber

El método de propiedad de [**la interfaz IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Parámetros**
</dt> <dd> <dl>

Parámetros de la máquina de fax.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parameters(
  [out] VARIANT* retval
);
HRESULT put_Parameters(
  [in] VARIANT vParameters
);
```


</dt> </dl> </dd> <dt>

**TelephoneNumber**
</dt> <dd> <dl>

Número de teléfono de la máquina de fax.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TelephoneNumber(
  [out] BSTR* retVal
);
HRESULT put_TelephoneNumber(
  [in] BSTR bstrTelephoneNumber
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
| IID<br/>                      | IID IADsFaxNumber se define como \_ A910DEA9-4680-11D1-0A3B-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[**ADS \_ FAXNUMBER**](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 






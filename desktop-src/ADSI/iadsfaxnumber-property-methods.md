---
title: Métodos de la propiedad IADsFaxNumber (iAds. h)
description: El método Property de la interfaz IADsFaxNumber establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
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
ms.openlocfilehash: 93e2d982aee794272f80e58385be34098a92a28e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658305"
---
# <a name="iadsfaxnumber-property-methods"></a>Métodos de propiedad IADsFaxNumber

El método Property de la interfaz [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber) establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Parámetros**
</dt> <dd> <dl>

Los parámetros del equipo de fax.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **variante**
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

Número de teléfono del equipo de fax.

<dt>

Tipo de acceso: lectura/escritura
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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsFaxNumber se define como A910DEA9-4680-11D1-0A3B-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)
</dt> <dt>

[**\_FAXNUMBER ADS**](/windows/win32/api/iads/ns-iads-ads_faxnumber)
</dt> </dl>

 

 






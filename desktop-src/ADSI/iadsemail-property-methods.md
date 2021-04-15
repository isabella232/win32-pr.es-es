---
title: Métodos de la propiedad IADsEmail (iAds. h)
description: El método Property de la interfaz IADsEmail establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 605ba62f-b15a-4411-839b-c4ad8acedd8a
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsEmail ADSI
topic_type:
- apiref
api_name:
- IADsEmail Property Methods
- IADsEmail.Type
- IADsEmail.get_Type
- IADsEmail.put_Type
- IADsEmail.Address
- IADsEmail.get_Address
- IADsEmail.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1956d5544b36cdaefcdd9d712ae99001d42279d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422518"
---
# <a name="iadsemail-property-methods"></a>Métodos de propiedad IADsEmail

El método Property de la interfaz [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail) establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Dirección**
</dt> <dd> <dl>

La dirección de correo electrónico del usuario.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] BSTR* retval
);
HRESULT put_Address(
  [in] BSTR bstrAddress
);
```


</dt> </dl> </dd> <dt>

**Tipo**
</dt> <dd> <dl>

El tipo del mensaje de correo electrónico.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Type(
  [out] LONG* retVal
);
HRESULT put_Type(
  [in] LONG lnType
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
| IID<br/>                      | IID \_ IADsEmail se define como 97AF011A-478E-11D1-A3B4-00C04FB950DC<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)
</dt> <dt>

[**\_correo electrónico de ADS**](/windows/win32/api/iads/ns-iads-ads_email)
</dt> </dl>

 

 






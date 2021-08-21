---
title: Métodos de propiedad IADsBackLink (Iads.h)
description: El método de propiedad de la interfaz IADsBackLink establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsBackLink ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2834ac74faa78418abfe1d960e4355aa6fa0c14999783ad9dfa47389f38eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691605"
---
# <a name="iadsbacklink-property-methods"></a>Métodos de propiedad IADsBackLink

El método de propiedad de [**la interfaz IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ObjectName**
</dt> <dd> <dl>

Nombre de un objeto al que está asociado el atributo **Back Link.**

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

**RemoteID**
</dt> <dd> <dl>

Identificador del servidor remoto que requiere una referencia externa del objeto especificado por **ObjectName**.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
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
| IID<br/>                      | IID \_ IADsBackLink se define como FD1302BD-4080-11D1-A3AC-00C04FB950DC<br/>         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[**ADS \_ BACKLINK**](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 






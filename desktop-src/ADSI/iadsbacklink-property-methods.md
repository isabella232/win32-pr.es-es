---
title: Métodos de la propiedad IADsBackLink (iAds. h)
description: El método Property de la interfaz IADsBackLink establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
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
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150778"
---
# <a name="iadsbacklink-property-methods"></a>Métodos de propiedad IADsBackLink

El método Property de la interfaz [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ObjectName**
</dt> <dd> <dl>

Nombre de un objeto al que está asociado el atributo de **vínculo hacia atrás** .

<dt>

Tipo de acceso: lectura/escritura
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

Identificador del servidor remoto que requiere una referencia externa del objeto especificado por **objectname**.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsBackLink se define como FD1302BD-4080-11D1-A3AC-00C04FB950DC<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[**\_BACKLINK ADS**](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 






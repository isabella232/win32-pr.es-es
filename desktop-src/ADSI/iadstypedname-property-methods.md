---
title: Métodos de la propiedad IADsTypedName (iAds. h)
description: El método Property de la interfaz IADsTypedName establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 0097c7c0-91f9-4874-93f2-c24900054a49
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsTypedName ADSI
topic_type:
- apiref
api_name:
- IADsTypedName Property Methods
- IADsTypedName.ObjectName
- IADsTypedName.get_ObjectName
- IADsTypedName.put_ObjectName
- IADsTypedName.Level
- IADsTypedName.get_Level
- IADsTypedName.put_Level
- IADsTypedName.Interval
- IADsTypedName.get_Interval
- IADsTypedName.put_Interval
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a90e3c3950fb3912e2fe206048053bec6322be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656527"
---
# <a name="iadstypedname-property-methods"></a>Métodos de propiedad IADsTypedName

El método Property de la interfaz [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname) establece la propiedad que se describe en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Intervalo**
</dt> <dd> <dl>

Frecuencia de referencia del objeto.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Interval(
  [out] LONG* retval
);
HRESULT put_Interval(
  [in] LONG lnInterval
);
```


</dt> </dl> </dd> <dt>

**Level**
</dt> <dd> <dl>

Nivel de prioridad asociado al objeto.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Level(
  [out] LONG* retval
);
HRESULT put_Level(
  [in] LONG lnLevel
);
```


</dt> </dl> </dd> <dt>

**ObjectName**
</dt> <dd> <dl>

Nombre de un objeto.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
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
| IID<br/>                      | IID \_ IADsTypedName se define como B371A349-4080-11D1-A3AC-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)
</dt> <dt>

[**\_TYPEDNAME ADS**](/windows/win32/api/iads/ns-iads-ads_typedname)
</dt> </dl>

 

 






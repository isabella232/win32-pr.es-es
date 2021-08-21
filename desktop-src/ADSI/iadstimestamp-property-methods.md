---
title: Métodos de propiedad IADsTimestamp (Iads.h)
description: El método de propiedad de la interfaz IADsTimestamp establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propiedad IADsTimestamp
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a105a2ba246c38b7cf6c5bdd1c7420096397e294bb29d5bed446b31d3ca9763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427573"
---
# <a name="iadstimestamp-property-methods"></a>Métodos de propiedad IADsTimestamp

El método de propiedad [**de la interfaz IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Id. de evento**
</dt> <dd> <dl>

Identificador de evento.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

**WholeSeconds**
</dt> <dd> <dl>

Número de segundos en los que el valor cero es 12:00 a. m., enero de 1970, HORA UTC.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
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
| IID<br/>                      | IID \_ IADsTimestamp se define como B2F5A901-4080-11D1-A3AC-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[**MARCA DE TIEMPO \_ DE ANUNCIOS**](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 






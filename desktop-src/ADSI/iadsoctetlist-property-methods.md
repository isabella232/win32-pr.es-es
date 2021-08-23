---
title: Métodos de propiedad IADsOctetList (Iads.h)
description: El método de propiedad de la interfaz IADsOctetList establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsOctetList ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa434eaf9cde95adb4b43d0261ac779d5183d9f3de2284704bc75cfa564521e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023443"
---
# <a name="iadsoctetlist-property-methods"></a>Métodos de propiedad IADsOctetList

El método de propiedad de [**la interfaz IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) establece la propiedad descrita en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**OctetList**
</dt> <dd> <dl>

Secuencia ordenada de matrices de bytes.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
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
| IID<br/>                      | IID \_ IADsOctetList se define como 7B28B80F-4680-11D1-A3B4-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[**ADS \_ OCTET \_ LIST**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 






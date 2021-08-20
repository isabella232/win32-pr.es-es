---
title: Métodos de propiedad IADsLargeInteger (Iads.h)
description: Los métodos de propiedad de la interfaz IADsLargeInteger obtienen y establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsLargeInteger ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b46a992accea468b6f3c8a70c7fcfcbe63cf72667c4394c27df273767a387b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023483"
---
# <a name="iadslargeinteger-property-methods"></a>Métodos de propiedad IADsLargeInteger

Los métodos de propiedad [**de la interfaz IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) obtienen y establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**HighPart**
</dt> <dd> <dl>

Parte alta del entero.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

**LowPart**
</dt> <dd> <dl>

Parte baja del entero.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentarios

Si largeInt es del tipo **LargeInteger,** su valor lo especifican los de **HighPart** y **LowPart** según la fórmula siguiente.


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a>Ejemplos

En el ejemplo Visual Basic código siguiente se establece un entero grande en 43937327281.


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsLargeInteger se define como 9068270B-0939-11D1-8BE1-00C04FD8D503<br/>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 






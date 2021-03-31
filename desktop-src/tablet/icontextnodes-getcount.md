---
description: Recupera el número de objetos IContextNode contenidos en esta colección.
ms.assetid: 7cc60bea-9a4c-4ac8-ad1a-0fca5e941c5e
title: 'IContextNodes:: GetCount (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNodes.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d694849b3436f9f30a687579362d01a111ace80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154429"
---
# <a name="icontextnodesgetcount-method"></a>IContextNodes:: GetCount (método)

Recupera el número de objetos [**IContextNode**](icontextnode.md) contenidos en esta colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pulCount* \[ enuncia\]
</dt> <dd>

Número de objetos [**IContextNode**](icontextnode.md) contenidos en esta colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 





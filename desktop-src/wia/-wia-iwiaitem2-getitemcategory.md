---
description: Obtiene la información de categoría de un elemento.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: Método IWiaItem2::GetItemCategory (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 958d5046e93dca4e5c90214bdb89803921ca507827c1134957db99fb70e3244f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034983"
---
# <a name="iwiaitem2getitemcategory-method"></a>IWiaItem2::GetItemCategory (método)

Obtiene la información de categoría de un elemento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItemCategoryGUID* \[ out\]
</dt> <dd>

Tipo: **\* GUID**

Recibe un puntero al GUID que identifica la categoría del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Cada [**objeto IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociado a un dispositivo de hardware Windows Image Acquisition (WIA) 2.0 tiene una categoría específica. Este método permite a las aplicaciones identificar la categoría de cualquier elemento de un árbol jerárquico de objetos de elemento en un dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 





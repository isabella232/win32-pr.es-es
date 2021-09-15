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
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575637"
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

## <a name="remarks"></a>Observaciones

Cada [**objeto IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociado a un dispositivo de hardware Windows Image Acquisition (WIA) 2.0 tiene una categoría específica. Este método permite a las aplicaciones identificar la categoría de cualquier elemento de un árbol jerárquico de objetos de elemento en un dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 





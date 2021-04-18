---
description: Obtiene la información de la categoría de un elemento.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'IWiaItem2:: GetItemCategory (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715191"
---
# <a name="iwiaitem2getitemcategory-method"></a>IWiaItem2:: GetItemCategory (método)

Obtiene la información de la categoría de un elemento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItemCategoryGUID* \[ enuncia\]
</dt> <dd>

Tipo: **GUID \** _

Recibe un puntero al GUID que identifica la categoría del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociados a un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0 tiene una categoría específica. Este método permite a las aplicaciones identificar la categoría de cualquier elemento en un árbol jerárquico de objetos de elemento en un dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 





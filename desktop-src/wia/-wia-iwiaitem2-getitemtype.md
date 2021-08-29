---
description: Obtiene la información de tipo de un elemento.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: Método IWiaItem2::GetItemType (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c71e88f951310c734924333ae1eab152f42baf830653c343f7b1af57422c079f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669697"
---
# <a name="iwiaitem2getitemtype-method"></a>IWiaItem2::GetItemType (método)

Obtiene la información de tipo de un elemento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItemType* \[ out\]
</dt> <dd>

Tipo: **\* LONG**

Recibe un puntero a **un long** que contiene una combinación de marcas de tipo. Vea [**MARCAS DE TIPO DE ELEMENTO DE WIA.**](-wia-wia-item-type-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Cada [**objeto IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociado a un dispositivo de hardware Windows Image Acquisition (WIA) 2.0 tiene un tipo de datos específico. Los objetos de elemento representan carpetas y archivos. Las carpetas contienen objetos de archivo. Los objetos de archivo contienen datos adquiridos por el dispositivo, como imágenes y sonidos. Este método permite a las aplicaciones identificar el tipo de cualquier elemento de un árbol jerárquico de objetos de elemento en un dispositivo.

Un elemento puede tener más de un tipo. Por ejemplo, un elemento que representa un archivo de audio tendrá los atributos de tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 





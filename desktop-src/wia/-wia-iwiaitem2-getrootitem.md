---
description: Obtiene el elemento raíz de un árbol de objetos de elemento que se usa para representar un dispositivo de hardware Windows adquisición de imágenes (WIA) 2.0.
ms.assetid: bc31ad4a-0851-4510-a038-83646ffd5c98
title: Método IWiaItem2::GetRootItem (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetRootItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c8d4f004cc9c7cabaf4898f5e8c838a0399dc106
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575636"
---
# <a name="iwiaitem2getrootitem-method"></a>IWiaItem2::GetRootItem (método)

Obtiene el elemento raíz de un árbol de objetos de elemento que se usa para representar un dispositivo de hardware Windows adquisición de imágenes (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRootItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Dado cualquier [**objeto IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2.0, la aplicación recupera un puntero al elemento raíz mediante una llamada a esta función.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro ppIWiaItem2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

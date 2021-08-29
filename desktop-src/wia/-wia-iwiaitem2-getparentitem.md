---
description: Obtiene el elemento primario del árbol que representa un Windows de hardware de adquisición de imágenes (WIA) 2.0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: Método IWiaItem2::GetParentItem (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetParentItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7b3ab6763cac004cea2b70e77f3bd750a22aad1d3950e3fc26d7f33664a69f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450405"
---
# <a name="iwiaitem2getparentitem-method"></a>IWiaItem2::GetParentItem (método)

Obtiene el elemento primario del árbol que representa un Windows de hardware de adquisición de imágenes (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) del elemento primario del árbol de objetos de elemento. Si se llama a este método en la raíz del árbol, la dirección devuelta es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Dado cualquier [**objeto IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2.0, la aplicación recupera un puntero al elemento primario llamando a esta función.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* si estos punteros no son **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

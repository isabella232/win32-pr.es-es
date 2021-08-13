---
description: Busca en el árbol de subelementos de un elemento con el nombre como clave de búsqueda.
ms.assetid: e4ce0bfb-9793-4928-b454-66ae1455b7b5
title: Método IWiaItem2::FindItemByName (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.FindItemByName
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 5ef0ffdf710d36d2d6c515352bf441e9c66ae169400528db5d5943e2114fefd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440413"
---
# <a name="iwiaitem2finditembyname-method"></a>IWiaItem2::FindItemByName (método)

Busca en el árbol de subelementos de un elemento con el nombre como clave de búsqueda.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FindItemByName(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrFullItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrFullItemName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del elemento que se buscará.

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) del elemento encontrado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método busca en el árbol de elementos del elemento actual con el nombre como clave de búsqueda. Si **IWiaItem2::FindItemByName** encuentra el elemento especificado por *bstrFullItemName*, almacena la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento en el *parámetro ppIWiaItem2.*

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

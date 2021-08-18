---
description: Crea una instancia adicional de la interfaz IEnumWiaItem2 y devuelve un puntero a ella.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: Método IEnumWiaItem2::Clone (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Clone
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 21c94c634a6930f28f48cdc35a4d3cf199b8fa33e9fb5f08444797fd76f50c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965854"
---
# <a name="ienumwiaitem2clone-method"></a>IEnumWiaItem2::Clone (Método)

Crea una instancia adicional de la [**interfaz IEnumWiaItem2**](-wia-ienumwiaitem2.md) y devuelve un puntero a ella.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recibe la dirección de la instancia de interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que **crea IEnumWiaItem2::Clone.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Las aplicaciones deben llamar [al método IUnknown::Release en](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) los punteros de interfaz que reciben a través del parámetro *ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

---
description: Crea una instancia adicional de la interfaz IEnumWiaItem2 y le devuelve un puntero.
ms.assetid: 0d36d555-d0d9-4a1c-ac54-de611850449c
title: 'IEnumWiaItem2:: Clone (método) (WIA. h)'
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
ms.openlocfilehash: 3279e7db3efe66e940adbcb9677204e5df7867f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810802"
---
# <a name="ienumwiaitem2clone-method"></a>IEnumWiaItem2:: Clone (método)

Crea una instancia adicional de la interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) y le devuelve un puntero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumWiaItem2 **ppIEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIEnum* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recibe la dirección de la instancia de la interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) que crea **IEnumWiaItem2:: Clone** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

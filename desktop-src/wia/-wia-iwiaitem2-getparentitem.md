---
description: Obtiene el elemento primario del árbol que representa un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: c6fdaf1d-9875-4852-893c-813894d89f6c
title: 'IWiaItem2:: GetParentItem (método) (WIA. h)'
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
ms.openlocfilehash: 055625b98807103c3b79109216f6081d00564b15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360332"
---
# <a name="iwiaitem2getparentitem-method"></a>IWiaItem2:: GetParentItem (método)

Obtiene el elemento primario del árbol que representa un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParentItem(
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppIWiaItem2* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento primario del elemento en el árbol de objetos de elemento. Si se llama a este método en la raíz del árbol, la dirección devuelta es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Dado cualquier objeto [**IWiaItem2**](-wia-iwiaitem2.md) en el árbol de objetos de un dispositivo de hardware WIA 2,0, la aplicación recupera un puntero al elemento primario llamando a esta función.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* si estos punteros no son **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

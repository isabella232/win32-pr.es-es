---
description: Crea un árbol jerárquico de objetos IWiaItem2 para un Windows image acquisition (WIA) 2.0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: Método IWiaDevMgr2::CreateDevice (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a40267e77671b807f0e6969845a3a5a7096694e4f4e7978467ee9ca5909284d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965734"
---
# <a name="iwiadevmgr2createdevice-method"></a>IWiaDevMgr2::CreateDevice (método)

Crea un árbol jerárquico [**de objetos IWiaItem2**](-wia-iwiaitem2.md) para un Windows image acquisition (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador único del dispositivo WIA 2.0.

</dd> <dt>

*ppWiaItem2Root* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz del árbol jerárquico del dispositivo WIA 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Las aplicaciones usan el método **IWiaDevMgr2::CreateDevice** para crear un objeto de dispositivo para los dispositivos WIA 2.0 especificados por el parámetro bstrDeviceID. Cuando vuelve, el método **IWiaDevMgr2::CreateDevice** almacena una dirección de un puntero en el parámetro *ppWiaItem2Root*, que apunta al elemento raíz del árbol de objetos [**IWiaItem2**](-wia-iwiaitem2.md) creado por **IWiaDevMgr2::CreateDevice**. Las aplicaciones pueden usar este árbol de objetos para controlar y recuperar datos del dispositivo WIA 2.0.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros que reciben a través del *parámetro ppWiaItem2Root.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 

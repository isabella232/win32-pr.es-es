---
description: Crea un árbol jerárquico de objetos IWiaItem2 para un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2:: CreateDevice (método) (WIA. h)'
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
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909870"
---
# <a name="iwiadevmgr2createdevice-method"></a>IWiaDevMgr2:: CreateDevice (método)

Crea un árbol jerárquico de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para un dispositivo de adquisición de imágenes de Windows (WIA) 2,0.

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

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrDeviceID* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el identificador único del dispositivo WIA 2,0.

</dd> <dt>

*ppWiaItem2Root* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recibe la dirección de un puntero a la interfaz [**IWiaItem2**](-wia-iwiaitem2.md) del elemento raíz en el árbol jerárquico para el dispositivo WIA 2,0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Las aplicaciones usan el método **IWiaDevMgr2:: CreateDevice** para crear un objeto de dispositivo para los dispositivos WIA 2,0 especificados por el parámetro bstrDeviceID. Cuando devuelve, el método **IWiaDevMgr2:: CreateDevice** almacena una dirección de un puntero en el parámetro *ppWiaItem2Root*, que señala al elemento raíz del árbol de objetos [**IWiaItem2**](-wia-iwiaitem2.md) creados por **IWiaDevMgr2:: CreateDevice**. Las aplicaciones pueden utilizar este árbol de objetos para controlar y recuperar datos del dispositivo WIA 2,0.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros que reciben a través del parámetro *ppWiaItem2Root* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 

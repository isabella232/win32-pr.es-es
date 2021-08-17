---
description: El método put \_ Hue especifica el valor de matiz en el que se va a claver. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ HUE.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: Método IDxtKey::p ut_Hue (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 063b8be8986a7a8a3fe3c7d14db31c0cb737d537b74366bee0ce3ed3550e3b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819452"
---
# <a name="idxtkeyput_hue-method"></a>Método IDxtKey::p ut \_ Hue

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Hue` método especifica el valor de matiz en el que se va a claver. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ HUE.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Valor de matiz en el que se va a claver. El intervalo válido es de 0 a 360.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDxtKey (interfaz)**](idxtkey.md)
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 





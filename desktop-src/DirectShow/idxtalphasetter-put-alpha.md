---
description: El \_ método Alpha Put especifica el valor alfa de toda la imagen.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: 'IDxtAlphaSetter: método de ut_Alpha de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 54bd69993a0dc0880f351f3e9ba7a79c9d926194
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690573"
---
# <a name="idxtalphasetterput_alpha-method"></a>IDxtAlphaSetter: \_ método alfa:p UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_Alpha` método especifica el valor alfa de toda la imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Alfa* \[ de\]
</dt> <dd>

Valor alfa. Este valor se aplicará a toda la imagen de destino. Para deshabilitar esta propiedad, establezca un valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si establece esta propiedad en un valor no negativo, también debe deshabilitar la propiedad de rampa alfa, llamando a **Put \_ AlphaRamp** con un valor negativo. De lo contrario, el efecto no se representará correctamente.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::p UT \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 





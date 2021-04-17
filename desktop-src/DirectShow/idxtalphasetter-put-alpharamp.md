---
description: El \_ método put AlphaRamp especifica la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen al 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter: método de ut_AlphaRamp de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691042"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>IDxtAlphaSetter::p \_ método AlphaRamp UT

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_AlphaRamp` método especifica la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen al 50%.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Alfa* \[ de\]
</dt> <dd>

La rampa alfa como un porcentaje. Por ejemplo, 1,0 es 100%. Para deshabilitar esta propiedad, establezca un valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si establece esta propiedad en un valor no negativo, también debe deshabilitar la propiedad alfa llamando a **Put \_ Alpha** con un valor negativo. De lo contrario, el efecto no se representará correctamente.

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

[**IDxtAlphaSetter::p el \_ alfa de UT**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 





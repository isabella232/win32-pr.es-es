---
description: El método \_ put AlphaRamp especifica la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen un 50 %.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: Método IDxtAlphaSetter::p ut_AlphaRamp (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375210"
---
# <a name="idxtalphasetterput_alpharamp-method"></a>Método \_ AlphaRamp :p IDxtAlphaSetter::p ut

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_AlphaRamp` método especifica la propiedad de rampa alfa. La rampa alfa es el porcentaje por el que se ajustan los valores alfa de la imagen original. Por ejemplo, si la rampa alfa es 0,5, los valores alfa de la imagen se reducen un 50 %.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Alfa* \[ En\]
</dt> <dd>

Rampa alfa como porcentaje. Por ejemplo, 1,0 es 100 %. Para deshabilitar esta propiedad, establezca un valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si establece esta propiedad en un valor no negativo, también debe deshabilitar la propiedad alfa mediante una llamada a **put \_ Alpha** con un valor negativo. De lo contrario, el efecto no se representará correctamente.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDxtAlphaSetter (interfaz)**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::put \_ Alpha**](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 





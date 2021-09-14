---
description: El método put \_ Alpha especifica el valor alfa para toda la imagen.
ms.assetid: ba02a9ae-b722-4771-89c6-e76369d39ed7
title: Método IDxtAlphaSetter::p ut_Alpha (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061089"
---
# <a name="idxtalphasetterput_alpha-method"></a>Método Alpha IDxtAlphaSetter::p ut \_

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Alpha` método especifica el valor alfa para toda la imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Alpha(
  [in] long Alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Alfa* \[ En\]
</dt> <dd>

Valor alfa. Este valor se aplicará a toda la imagen de destino. Para deshabilitar esta propiedad, establezca un valor negativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si establece esta propiedad en un valor no negativo, también debe deshabilitar la propiedad de rampa alfa mediante una llamada a **put \_ AlphaRamp** con un valor negativo. De lo contrario, el efecto no se representará correctamente.

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

[**Interfaz IDxtAlphaSetter**](idxtalphasetter.md)
</dt> <dt>

[**IDxtAlphaSetter::put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md)
</dt> </dl>

 

 





---
description: El \_ método get Alpha recupera el valor alfa de toda la imagen.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Método IDxtAlphaSetter:: get_Alpha (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690380"
---
# <a name="idxtalphasetterget_alpha-method"></a>IDxtAlphaSetter:: get \_ Alpha (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_Alpha` método recupera el valor alfa de toda la imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Recibe el valor alfa. Este valor alfa se aplicará a toda la imagen de destino. Un valor negativo indica que no se ha establecido ningún valor alfa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                               | Descripción                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_puntero E**</dt> </dl> | Argumento de puntero **nulo**<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto<br/>                   |



 

## <a name="remarks"></a>Observaciones

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
</dt> </dl>

 

 





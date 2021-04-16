---
description: El \_ método get RGB recupera el color RGB en el que se va a incluir la tecla. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Método IDxtKey:: get_RGB (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679418"
---
# <a name="idxtkeyget_rgb-method"></a>IDxtKey:: get \_ RGB (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_RGB` método recupera el color RGB en el que se va a hacer la tecla. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe el color. El valor devuelto es un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

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

[**Interfaz IDxtKey**](idxtkey.md)
</dt> <dt>

[**IDxtKey:: get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 





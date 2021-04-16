---
description: El \_ método put Hue especifica el valor de matiz que se va a incluir en la clave. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ Hue.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'IDxtKey: método de ut_Hue de:p (QEDIT. h)'
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
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679415"
---
# <a name="idxtkeyput_hue-method"></a>IDxtKey::p \_ método Hue

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_Hue` método especifica el valor de matiz en el que se va a especificar la tecla. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ Hue.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Valor de matiz en el que se va a hacer la tecla. El intervalo válido es de 0 a 360.

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

[**IDxtKey::p \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 





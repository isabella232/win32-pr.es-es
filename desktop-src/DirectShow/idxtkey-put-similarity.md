---
description: El \_ método put similitud especifica el intervalo de datos de color que se vuelve transparente. En los valores más altos, una mayor variedad de colores similares es transparente. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey: método de ut_Similarity de:p (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680495"
---
# <a name="idxtkeyput_similarity-method"></a>IDxtKey: método de similitud de:p UT \_

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `put_Similarity` método especifica el intervalo de datos de color que se vuelve transparente. En los valores más altos, una mayor variedad de colores similares es transparente. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ de\]
</dt> <dd>

Especifica el valor de similitud. El intervalo válido es de 0 a 100.

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

 

 





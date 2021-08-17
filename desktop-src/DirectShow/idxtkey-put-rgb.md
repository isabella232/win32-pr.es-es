---
description: El método \_ PUT RGB especifica el color RGB en el que se va a claver. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: Método IDxtKey::p ut_RGB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f53cb5d856377b611c5ea90d3b9c1f7fa522d892e6c79aa50d350883497398a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819398"
---
# <a name="idxtkeyput_rgb-method"></a>Método RGB IDxtKey::p ut \_

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_RGB` método especifica el color RGB en el que se va a claver. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Especifica el color como un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.

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

 

 





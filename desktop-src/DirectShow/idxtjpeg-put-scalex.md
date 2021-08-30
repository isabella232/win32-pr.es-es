---
description: El método \_ put ScaleX especifica la cantidad por la que el borrado se ajusta horizontalmente.
ms.assetid: d57af5dc-41e0-45a7-8f11-55ef3bc62549
title: Método IDxtAsynceg::p ut_ScaleX (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b22a02f643d4e9c44b6bb407da4e974469531295c208a1e004be5cee1801f0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042875"
---
# <a name="idxtjpegput_scalex-method"></a>Método ScaleX :p \_ IDxtAsynceg::p ut

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_ScaleX` método especifica la cantidad por la que se extiende horizontalmente el borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ScaleX(
  [in] double newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Cantidad por la que el borrado se extiende horizontalmente, como porcentaje de la definición de borrado original. Por ejemplo, el valor 1,0 significa que no hay stretching y 2,0 significa un 200 % de stretching.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDxt Jpeg (interfaz)**](idxtjpeg.md)
</dt> </dl>

 

 





---
description: El método \_ get ScaleY recupera la cantidad por la que el borrado se ajusta verticalmente.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: Método IDxtAsynceg::get_ScaleY (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3da97c829c8234a5bd0e8c9b82bf9a7f3334bca78de395be2e5724d8a52f4838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639405"
---
# <a name="idxtjpegget_scaley-method"></a>Método IDxtAsynceg::get \_ ScaleY

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_ScaleY` método recupera la cantidad por la que se extiende verticalmente el borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe la cantidad por la que el borrado se extiende verticalmente, como porcentaje de la definición de borrado original. Por ejemplo, el valor 1,0 significa que no hay stretching y 2,0 significa un 200 % de stretching.

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

 

 





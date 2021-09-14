---
description: El método \_ get ScaleX recupera la cantidad por la que el borrado se ajusta horizontalmente.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: Método IDxtAsynceg::get_ScaleX (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061071"
---
# <a name="idxtjpegget_scalex-method"></a>IDxtAsynceg::get \_ ScaleX (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_ScaleX` método recupera la cantidad por la que se extiende horizontalmente el borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe la cantidad por la que el borrado se extiende horizontalmente, como un porcentaje de la definición de borrado original. Por ejemplo, el valor 1,0 significa que no hay stretching y 2,0 significa un 200 % de extensión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDxtEnceeg (interfaz)**](idxtjpeg.md)
</dt> </dl>

 

 





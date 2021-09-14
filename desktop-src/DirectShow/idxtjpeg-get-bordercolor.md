---
description: El método \_ get BorderColor recupera el color del borde alrededor de los bordes del patrón de borrado.
ms.assetid: 9d36cc49-c174-4b93-a030-ca8d2890c624
title: Método IDxtAsynceg::get_BorderColor (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_BorderColor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7f37c37865caf76839733ada376ec637747977ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061084"
---
# <a name="idxtjpegget_bordercolor-method"></a>IDxtAsynceg::get \_ BorderColor (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_BorderColor` método recupera el color del borde alrededor de los bordes del patrón de borrado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_BorderColor(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el color. El valor devuelto es un número hexadecimal con el formato 0xRRGGBB, donde RR es el valor rojo, GG es el valor verde y BB es el valor azul.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

[**IDxtEnceeg (interfaz)**](idxtjpeg.md)
</dt> </dl>

 

 





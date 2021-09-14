---
description: El método get InputSize devuelve el tamaño de entrada actual del filtro de cambio \_ de tamaño.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: Método IResize::get_InputSize (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891788"
---
# <a name="iresizeget_inputsize-method"></a>Método IResize::get \_ InputSize

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método devuelve el tamaño de entrada actual del `get_InputSize` filtro de cambio de tamaño.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piHeight* \[ out\]
</dt> <dd>

Recibe el alto del vídeo, en píxeles.

</dd> <dt>

*piWidth* \[ out\]
</dt> <dd>

Recibe el ancho del vídeo, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si el pin de entrada del filtro no está conectado, devuelva un código de error. De lo contrario, devuelva el ancho y el alto del vídeo, tal y como especifica el tipo de medio de la patilla de entrada.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> <dt>

[**IResize (Interfaz)**](iresize.md)
</dt> </dl>

 

 





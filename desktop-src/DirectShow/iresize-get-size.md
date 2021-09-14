---
description: El método get \_ Size devuelve el tamaño de salida actual y el modo de ajuste.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: Método IResize::get_Size (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b9fe4971fd9ede0f695fe06a4102da8243e7c720
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891748"
---
# <a name="iresizeget_size-method"></a>IResize::get \_ Size (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_Size` método devuelve el tamaño de salida actual y el modo de ajuste.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
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

</dd> <dt>

*pFlag* \[ out\]
</dt> <dd>

Recibe una marca que especifica el modo de ajuste. Vea [**Cambiar el tamaño de las marcas**](resize-flags.md) para ver los valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Si no se ha establecido el tipo de salida, el filtro debe devolver los valores predeterminados. Estos valores se pueden elegir arbitrariamente en tiempo de diseño.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9.0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**IResize (Interfaz)**](iresize.md)
</dt> </dl>

 

 





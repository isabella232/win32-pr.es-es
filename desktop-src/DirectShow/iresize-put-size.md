---
description: El método put \_ Size establece el tamaño de salida y el modo de ajuste.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: Método IResize::p ut_Size (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891732"
---
# <a name="iresizeput_size-method"></a>Método IResize::p ut \_ Size

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Size` método establece el tamaño de salida y el modo de ajuste.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Alto* \[ En\]
</dt> <dd>

Alto del vídeo, en píxeles.

</dd> <dt>

*Ancho* \[ En\]
</dt> <dd>

Ancho del vídeo, en píxeles.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Modo de ajuste. Consulte [**Cambiar el tamaño de las marcas**](resize-flags.md) para ver los valores posibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

DES puede llamar a este método antes o después de llamar a **put \_ MediaType**. Si DES llama a este método antes de llamar a **put \_ MediaType**, el filtro debe seleccionar un valor predeterminado para la profundidad de bits y usar los valores de tamaño para construir un tipo de medio de salida. Si DES llama a este método después de llamar a **put \_ MediaType**, el filtro debe modificar su tipo de salida actual con los nuevos tamaños.

DES también puede llamar a este método una vez conectada la marca de salida. En ese caso, modifique el tipo de salida y vuelva a conectar el pin de salida con el nuevo tipo. Consulte [Volver a conectar los pins](reconnecting-pins.md) para obtener más información.

El *parámetro Flags* especifica cómo debe realizar el filtro la operación de tamaño.

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

 

 





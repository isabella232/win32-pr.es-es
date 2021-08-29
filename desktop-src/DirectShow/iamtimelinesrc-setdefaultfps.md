---
description: El método SetDefaultFPS establece la velocidad de fotogramas predeterminada del objeto de origen.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: Método IAMTimelineSrc::SetDefaultFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5eda06b5aeb327de21b72332cd26a71884369b9c4171e1b0611f0e6259f9c1ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915015"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>Método IAMTimelineSrc::SetDefaultFPS

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método establece la velocidad de fotogramas predeterminada `SetDefaultFPS` del objeto de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FPS* 
</dt> <dd>

Velocidad de fotogramas predeterminada, en fotogramas por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E \_ INVALIDARG si la velocidad de fotogramas especificada es menor que cero.

## <a name="remarks"></a>Comentarios

El motor de representación usa este valor si no puede determinar la velocidad de fotogramas del archivo de origen original.

Llame a este método solo para los archivos de código fuente sin una velocidad de fotogramas predefinida. En el caso de los archivos JPEG y de mapa de bits, la velocidad de fotogramas predeterminada es cero, lo que hace que el origen se represente como una imagen fija. Para usar la imagen como primer fotograma de una secuencia DIB, establezca la velocidad de fotogramas en un valor mayor que cero. Para obtener más información, [vea Trabajar con orígenes](working-with-sources.md).

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método SetDefaultFPS establece la velocidad de fotogramas predeterminada del objeto de origen.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'IAMTimelineSrc:: SetDefaultFPS (método) (QEDIT. h)'
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
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680572"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a>IAMTimelineSrc:: SetDefaultFPS (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetDefaultFPS` método establece la velocidad de fotogramas predeterminada del objeto de origen.

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

Devuelve S \_ correcto si es correcto, o E \_ INVALIDARG si la velocidad de fotogramas especificada es menor que cero.

## <a name="remarks"></a>Observaciones

El motor de representación utiliza este valor si no puede determinar la velocidad de fotogramas del archivo de código fuente original.

Llame a este método solo para los archivos de código fuente sin una velocidad de fotogramas predefinida. En el caso de los archivos de mapa de bits y JPEG, la velocidad de fotogramas predeterminada es cero, lo que hace que el origen se represente como una imagen fija. Para usar la imagen como primer fotograma en una secuencia DIB, establezca la velocidad de fotogramas en un valor mayor que cero. Para obtener más información, vea [trabajar con orígenes](working-with-sources.md).

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

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





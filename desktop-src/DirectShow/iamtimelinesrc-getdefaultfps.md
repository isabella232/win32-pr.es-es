---
description: El método GetDefaultFPS recupera la velocidad de fotogramas predeterminada del objeto de origen. El motor de representación utiliza este valor si no puede determinar la velocidad de fotogramas del origen original.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'IAMTimelineSrc:: GetDefaultFPS (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689965"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>IAMTimelineSrc:: GetDefaultFPS (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetDefaultFPS` método recupera la velocidad de fotogramas predeterminada del objeto de origen. El motor de representación utiliza este valor si no puede determinar la velocidad de fotogramas del origen original.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFPS* 
</dt> <dd>

Recibe la velocidad de fotogramas predeterminada, en fotogramas por segundo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La velocidad de fotogramas predeterminada no es necesaria si el formato de archivo especifica la velocidad de fotogramas. Este es el caso de los formatos de audio y vídeo.

Si el origen es un mapa de bits o una imagen JPEG, el motor de representación lo usa como la primera imagen en una secuencia de mapa de bits independiente del dispositivo (DIB), con una velocidad de fotogramas igual a la velocidad de fotogramas predeterminada. Para representar una imagen estática, en lugar de una secuencia DIB, establezca la velocidad de fotogramas predeterminada en 0.

Si el origen es un archivo GIF, no establezca la velocidad de fotogramas. En el caso de los GIF animados, el archivo GIF especifica el retraso entre cada imagen.

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

 

 





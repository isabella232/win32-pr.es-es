---
description: El método GetDefaultFPS recupera la velocidad de fotogramas predeterminada del objeto de origen. El motor de representación usa este valor si no puede determinar la velocidad de fotogramas del origen original.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: Método IAMTimelineSrc::GetDefaultFPS (Qedit.h)
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
ms.openlocfilehash: 92154a4c97c46307a764a7dba22ff2e003621db59cdb962ff025635022a5384b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131215"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a>Método IAMTimelineSrc::GetDefaultFPS

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera la velocidad de fotogramas predeterminada `GetDefaultFPS` del objeto de origen. El motor de representación usa este valor si no puede determinar la velocidad de fotogramas del origen original.

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

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La velocidad de fotogramas predeterminada no es necesaria si el formato de archivo especifica la velocidad de fotogramas. Este es el caso de los formatos de audio y vídeo.

Si el origen es un mapa de bits o una imagen JPEG, el motor de representación la usa como la primera imagen de una secuencia de mapa de bits independiente del dispositivo (DIB), con una velocidad de fotogramas igual a la velocidad de fotogramas predeterminada. Para representar una imagen estática, en lugar de una secuencia DIB, establezca la velocidad de fotogramas predeterminada en 0.

Si el origen es un GIF, no establezca la velocidad de fotogramas. En el caso de los GIF animados, el archivo GIF especifica el retraso entre cada imagen.

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

 

 





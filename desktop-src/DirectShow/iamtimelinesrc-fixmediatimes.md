---
description: El método FixMediaTimes redondea los valores de tiempo especificados al límite de fotogramas más cercano, tal como se define en la velocidad de fotogramas de salida. En general, las aplicaciones no necesitan llamar a este método.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: Método IAMTimelineSrc::FixMediaTimes (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dcace4e501a27b1f82b148533f382f5c86bafb17d9bf34343f1e43a8893672c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052405"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>IamTimelineSrc::FixMediaTimes (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `FixMediaTimes` método redondea los valores de tiempo especificados al límite de fotogramas más cercano, tal como se define en la velocidad de fotogramas de salida. En general, las aplicaciones no necesitan llamar a este método.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio, en unidades de 100 nanosegundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que contiene la hora de detenerse, en unidades de 100 nanosegundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método es similar al [**método IAMTimelineObj::FixTimes,**](iamtimelineobj-fixtimes.md) pero conserva la proporción original de tiempos multimedia y de escala de tiempo. Simplemente redondear los tiempos al límite de fotograma más cercano podría distorsionar esta proporción.

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

 

 





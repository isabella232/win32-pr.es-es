---
description: El método FixMediaTimes2 redondea los valores de tiempo especificados al límite de fotogramas más cercano, tal como se define en la velocidad de fotogramas de salida. Este método es equivalente a IAMTimelineSrc::FixMediaTimes, pero toma valores REFTIME.
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: Método IAMTimelineSrc::FixMediaTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ceff01e17d82ed59e8d63811841e58e97323a9be4ec4c40b719bb655aac464e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399625"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a>Método IAMTimelineSrc::FixMediaTimes2

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `FixMediaTimes2` método redondea los valores de tiempo especificados al límite de fotogramas más cercano, tal como se define en la velocidad de fotogramas de salida. Este método es equivalente a [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), pero toma [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Puntero a una variable que contiene la hora de inicio, en segundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> <dt>

*pStop* 
</dt> <dd>

Puntero a una variable que contiene el tiempo de detenerse, en segundos. Si la llamada se realiza correctamente, esta variable se establece en el tiempo redondeado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





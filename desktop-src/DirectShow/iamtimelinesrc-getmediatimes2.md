---
description: El método GetMediaTimes2 recupera las horas de inicio y de detenerse de los medios. Este método es equivalente a IAMTimelineSrc::GetMediaTimes, pero toma valores REFTIME.
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: Método IAMTimelineSrc::GetMediaTimes2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160152"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a>IamTimelineSrc::GetMediaTimes2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetMediaTimes2` método recupera las horas de inicio y de detenerse de los medios. Este método es equivalente a [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), pero toma [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Recibe la hora de inicio del medio, en segundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recibe el tiempo de detenerse del medio, en segundos.

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

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





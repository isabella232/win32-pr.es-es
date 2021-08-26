---
description: El método SplitAt2 divide el objeto en el momento especificado. Este método es equivalente a IAMTimelineSplittable::SplitAt, pero toma un valor REFTIME.
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: Método IAMTimelineSplittable::SplitAt2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9c3a5720ade42291037611c155c2cb9e834f0734e7af6e2c36277c409592143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904915"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>IamTimelineSplittable::SplitAt2 (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SplitAt2` método divide el objeto en el momento especificado. Este método es equivalente a [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), pero toma un [**valor REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Time* 
</dt> <dd>

Hora a la que se va a dividir el objeto, en relación con el inicio de la escala de tiempo, en segundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | No hay nada que dividir.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El objeto no existe en este momento.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                    |



 

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineSplittable (interfaz)**](iamtimelinesplittable.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





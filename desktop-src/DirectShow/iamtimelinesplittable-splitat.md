---
description: El método SplitAt divide el objeto en el momento especificado.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: Método IAMTimelineSplittable::SplitAt (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cdcedc25cf7f0998c6eac11de63f6e0d329e2ca8500576e0ad9e69cfc0bb3067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052415"
---
# <a name="iamtimelinesplittablesplitat-method"></a>IamTimelineSplittable::SplitAt (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SplitAt` método divide el objeto en el momento especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Time* 
</dt> <dd>

Hora a la que se va a dividir el objeto, en relación con el inicio de la escala de tiempo, en unidades de 100 nanosegundos.

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

Si divide un origen, efecto o transición, este método crea un segundo objeto del mismo tipo. El objeto original se trunca en el tiempo de división especificado y el nuevo objeto reemplaza la parte truncada. El nuevo objeto hereda todas las mismas propiedades. En un objeto de origen, el método también divide los efectos que se incluyen en el tiempo de división.

Al llamar a este método en una pista, se dividen todos los orígenes, efectos y transiciones contenidos en la pista en el tiempo de división especificado. No crea una segunda pista. (Una pista comienza en el momento cero y se extiende al infinito).

Para una pista, si el tiempo de división es posterior a todo en la pista, el método devuelve S \_ FALSE. Para cualquier otro objeto, si el tiempo de división no se encuentra en ningún lugar dentro del objeto , el método devuelve E \_ INVALIDARG.

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

 

 





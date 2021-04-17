---
description: El método SplitAt divide el objeto en el momento especificado.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'IAMTimelineSplittable:: SplitAt (método) (QEDIT. h)'
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
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690546"
---
# <a name="iamtimelinesplittablesplitat-method"></a>IAMTimelineSplittable:: SplitAt (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

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

Hora a la que se va a dividir el objeto, en relación con el inicio de la escala de tiempo, en unidades de 100-nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Nada para dividir.<br/>                       |
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El objeto no existe en este momento.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Si divide un origen, un efecto o una transición, este método crea un segundo objeto del mismo tipo. El objeto original se trunca en el tiempo de división especificado y el nuevo objeto reemplaza la parte truncada. El nuevo objeto hereda todas las propiedades. En un objeto de origen, el método también divide los efectos que se encuentran en el tiempo de división.

La llamada a este método en una pista divide todos los orígenes, efectos y transiciones contenidos en la pista en el tiempo de división especificado. No crea una segunda pista. (Una pista comienza en el tiempo cero y se extiende hasta el infinito).

En el caso de una pista, si el tiempo de división es posterior a todo lo que hay en la pista, el método devuelve S \_ false. Para cualquier otro objeto, si el tiempo de división no se encuentra en ningún lugar dentro del objeto, el método devuelve E \_ INVALIDARG.

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

[**Interfaz IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





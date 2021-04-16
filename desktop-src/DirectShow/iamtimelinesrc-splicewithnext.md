---
description: El método SpliceWithNext une el objeto de origen a otro objeto de origen.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'IAMTimelineSrc:: SpliceWithNext (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690079"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>IAMTimelineSrc:: SpliceWithNext (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SpliceWithNext` método une el objeto de origen a otro objeto de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pNext* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen que se va a combinar con el origen actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los posibles valores devueltos se incluyen los siguientes:



| Código devuelto                                                                                   | Descripción                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>                                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | El objeto especificado por el parámetro *pNext* no es un objeto de origen.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Argumento de puntero **nulo** .<br/>                                    |



 

## <a name="remarks"></a>Observaciones

Tal y como se implementa actualmente, este método descarta cualquier efecto en *pNext*.

Para que este método se ejecute correctamente, *pNext* debe ser un marco de coincidencia del objeto de origen actual, definido como se indica a continuación:

-   Debe compartir el mismo archivo de código fuente.
-   La hora de inicio del medio debe ser igual a la hora de detención del medio del origen actual.
-   La velocidad de reproducción debe ser la misma. La velocidad de reproducción es la duración multimedia dividida por la duración de la escala de tiempo.

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

 

 





---
description: El método GetCountOfType recupera de forma recursiva el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: Método IAMTimelineComp::GetCountOfType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b0504a7adb41a0d6a45714090a39aeefda9a3ef53b2d834540f600ec3ef871a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756415"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>IamTimelineComp::GetCountOfType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera de forma recursiva el número de objetos de un tipo determinado contenidos en esta composición y todas sus `GetCountOfType` pistas virtuales.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe de forma recursiva el número de objetos del tipo especificado contenidos en esta composición y todas sus pistas virtuales.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recibe el recuento devuelto en *pVal más* el número de composiciones buscadas, incluida esta.

</dd> <dt>

*MajorType* 
</dt> <dd>

Miembro del tipo [**enumerado TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) especificando el tipo de objeto que se debe contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E POINTER en caso \_ contrario.

## <a name="remarks"></a>Comentarios

Normalmente, una aplicación no llamará a este método. Lo llama el motor de representación.

Si cuenta las composiciones, el valor devuelto en *pVal* es cero y el valor devuelto en *pValWithComps* es el número de composiciones. El valor de *\* pValWithComps* incluye la composición en la que se llama al método . Por ejemplo, si llama a este método en una composición vacía, *\* pValWithComps* es igual a 1.

Los grupos no pueden residir en composiciones, por lo que no se puede usar este método para contar grupos. (El recuento devuelto siempre será cero). Para contar grupos, llame al [**método IAMTimeline::GetGroupCount.**](iamtimeline-getgroupcount.md)

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

[**IamTimelineComp (interfaz)**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





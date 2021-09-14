---
description: El método GetCountOfType recupera el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.
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
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892177"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>IamTimelineComp::GetCountOfType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera el número de objetos de un tipo determinado contenido en esta composición y todas sus pistas `GetCountOfType` virtuales, de forma recursiva.

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

Recibe el número de objetos del tipo especificado contenido en esta composición y todas sus pistas virtuales de forma recursiva.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recibe el recuento devuelto en *pVal más* el número de composiciones buscadas, incluida esta.

</dd> <dt>

*MajorType* 
</dt> <dd>

Miembro del tipo [**enumerado \_ TIMELINE MAJOR \_ TYPE,**](timeline-major-type.md) especificando el tipo de objeto que se debe contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o E POINTER en caso \_ contrario.

## <a name="remarks"></a>Observaciones

Normalmente, una aplicación no llamará a este método. Lo llama el motor de representación.

Si cuenta las composiciones, el valor devuelto en *pVal* es cero y el valor devuelto en *pValWithComps* es el número de composiciones. El valor de *\* pValWithComps* incluye la composición en la que se llama al método . Por ejemplo, si llama a este método en una composición vacía, *\* pValWithComps* es igual a 1.

Los grupos no pueden residir dentro de composiciones, por lo que no se puede usar este método para contar grupos. (El recuento devuelto siempre será cero). Para contar grupos, llame al [**método IAMTimeline::GetGroupCount.**](iamtimeline-getgroupcount.md)

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IAMTimelineComp (Interfaz)**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





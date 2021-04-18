---
description: El método GetCountOfType recupera el número de objetos de un tipo determinado incluido en esta composición y todas sus pistas virtuales de forma recursiva.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'IAMTimelineComp:: GetCountOfType (método) (QEDIT. h)'
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680975"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>IAMTimelineComp:: GetCountOfType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetCountOfType` método recupera el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.

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

Recibe el número de objetos del tipo especificado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recibe el recuento devuelto en *pval* más el número de composiciones buscadas, incluido este.

</dd> <dt>

*MajorType* 
</dt> <dd>

Miembro del tipo [**\_ principal \_**](timeline-major-type.md) de la escala de tiempo, que especifica el tipo de objeto que se va a contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve \_ si es correcto, o bien el puntero E, de \_ lo contrario.

## <a name="remarks"></a>Observaciones

Normalmente, una aplicación no llamará a este método. Lo llama el motor de representación.

Si cuenta las composiciones, el valor devuelto en *pval* es cero y el valor devuelto en *pValWithComps* es el número de composiciones. El valor de *\* pValWithComps* incluye la composición en la que se llama al método. Por ejemplo, si llama a este método en una composición vacía, *\* pValWithComps* es igual a 1.

Los grupos no pueden residir en composiciones, por lo que no puede usar este método para contar grupos. (El recuento devuelto siempre será cero). Para contar los grupos, llame al método [**IAMTimeline:: GetGroupCount**](iamtimeline-getgroupcount.md) .

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

[**Interfaz IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





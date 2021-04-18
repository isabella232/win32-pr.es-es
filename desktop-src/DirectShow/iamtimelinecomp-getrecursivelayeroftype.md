---
description: El método GetRecursiveLayerOfType realiza una ordenación con prioridad a la profundidad de las pistas virtuales contenidas en esta composición y recupera la pista virtual n de esa ordenación.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'IAMTimelineComp:: GetRecursiveLayerOfType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680972"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>IAMTimelineComp:: GetRecursiveLayerOfType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetRecursiveLayerOfType` método realiza una ordenación con prioridad a la profundidad de las pistas virtuales contenidas en esta composición y recupera la *n*-ésima pista virtual de esa ordenación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVirtualTrack* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.

</dd> <dt>

*WhichLayer* 
</dt> <dd>

Especifica la pista virtual que se va a recuperar, indizada desde cero.

</dd> <dt>

*Tipo* 
</dt> <dd>

Miembro del tipo enumerado de [**\_ \_ tipo principal**](timeline-major-type.md) de la escala de tiempo que especifica si se deben incluir pistas en la búsqueda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                  | Descripción                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | No hay ningún objeto del tipo especificado.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/>       |



 

## <a name="remarks"></a>Observaciones

Normalmente, una aplicación no necesita llamar a este método.

Si el parámetro de *tipo* es la \_ pista de tipo principal de la escala de tiempo \_ \_ , la ordenación con prioridad a la profundidad incluye pistas. En caso contrario, solo incluye composiciones y grupos. El propio objeto se incluye en el orden.

Por ejemplo, en la siguiente disposición, a partir de la composición A, el orden sería B, C, F, D, E, A.

![getrecursivelayeroftype](images/composition.png)

Si el método se ejecuta correctamente, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

 

 





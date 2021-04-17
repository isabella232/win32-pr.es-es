---
description: El método VTrackInsBefore inserta una pista virtual en la composición con la prioridad especificada.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'IAMTimelineComp:: VTrackInsBefore (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680969"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>IAMTimelineComp:: VTrackInsBefore (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `VTrackInsBefore` método inserta una pista virtual en la composición con la prioridad especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.

</dd> <dt>

*Prioridad* 
</dt> <dd>

Prioridad con la que se va a insertar la pista virtual, o – 1 para insertar la pista virtual al final de la lista de prioridades. La lista prioridad determina qué clips están visibles. Vea Comentarios para obtener más información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                   | Descripción                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | El objeto no es una pista virtual.<br/> |



 

## <a name="remarks"></a>Observaciones

Cada pista virtual de la composición tiene un nivel de prioridad único. Los niveles de prioridad van de 0 a *n* -1, donde *n* es el número de pistas virtuales en la composición. En el caso de los grupos de vídeo, una pista virtual oculta cualquier pista virtual con un nivel de prioridad inferior, excepto en los lugares donde la pista está vacía o contiene una transición. Puede considerar las pistas virtuales como capas en la composición final. El seguimiento 1 está superpuesto a la pista 0, el seguimiento 2 se superpone a la pista 1, y así sucesivamente.

Si especifica-1 para el parámetro *Priority* , la pista virtual se inserta al final de la lista, con un valor de prioridad mayor que el de las pistas existentes. Si especifica un valor de prioridad que ya existe en la composición, cada pista con una prioridad igual o mayor sube un nivel de prioridad.

**Ejemplo**: Track A tiene prioridad 0 y Track B tiene prioridad 1. Si el seguimiento C se inserta en la prioridad 0, el seguimiento de se desplaza a la prioridad 1 y el seguimiento de B se desplaza a la prioridad 2.

Si la prioridad especificada es mayor que el número actual de pistas en la composición, se produce un error en el método.

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

 

 





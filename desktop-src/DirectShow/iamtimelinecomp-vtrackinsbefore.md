---
description: El método VTrackInsBefore inserta una pista virtual en la composición con la prioridad especificada.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: Método IAMTimelineComp::VTrackInsBefore (Qedit.h)
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
ms.openlocfilehash: c84038dcaaed7fe56c06d195e269c4bb03f1c18a58b4ec4490dc8cae541b9a54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928365"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>IamTimelineComp::VTrackInsBefore (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

Puntero a la [**interfaz IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.

</dd> <dt>

*Prioridad* 
</dt> <dd>

Prioridad en la que se va a insertar la pista virtual, o –1 para insertar la pista virtual al final de la lista de prioridad. La lista de prioridad determina qué clips están visibles. Vea Comentarios para obtener más información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                   | Descripción                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento no válido.<br/>              |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | El objeto no es una pista virtual.<br/> |



 

## <a name="remarks"></a>Comentarios

Cada pista virtual en composición tiene un nivel de prioridad único. Los niveles de prioridad van de 0 a *n* - 1, donde *n* es el número de pistas virtuales en la composición. En el caso de los grupos de vídeos, una pista virtual oculta las pistas virtuales con un nivel de prioridad inferior, excepto en los lugares donde la pista está vacía o contiene una transición. Puede pensar que las pistas virtuales son capas en la composición final. La pista 1 está en capas sobre la pista 0, la pista 2 se en capas sobre la pista 1, etc.

Si especifica -1 para el parámetro *Priority,* la pista virtual se inserta al final de la lista, con un valor de prioridad más alto que las pistas existentes. Si especifica un valor de prioridad que ya existe en la composición, cada pista con una prioridad igual o mayor subirá un nivel de prioridad.

**Ejemplo:** el seguimiento A tiene prioridad 0 y el seguimiento B tiene prioridad 1. Si la pista C se inserta en la prioridad 0, la pista A pasa a la prioridad 1 y la pista B pasa a la prioridad 2.

Si la prioridad especificada es mayor que el número actual de pistas de la composición, se produce un error en el método.

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

[**IAMTimelineComp (Interfaz)**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





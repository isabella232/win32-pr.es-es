---
description: El método SrcAdd agrega un origen a la pista.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: Método IAMTimelineTrack::SrcAdd (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e705f840a073ee6796776f6f68c7b57df0bd972facf8f7a586792519735bfb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998755"
---
# <a name="iamtimelinetracksrcadd-method"></a>IAMTimelineTrack::SrcAdd (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SrcAdd` método agrega un origen a la pista.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj del**](iamtimelineobj.md) objeto de origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente. Devuelve E \_ NOINTERFACE si el objeto no es un objeto de origen. De lo contrario, devuelve **un valor HRESULT** que indica la causa del error.

## <a name="remarks"></a>Comentarios

Establezca las horas de inicio y de detenerse del origen antes de llamar a este método. (Llame [**a IAMTimelineObj::SetStartStop).**](iamtimelineobj-setstartstop.md)

Actualmente, DES no puede representar simultáneamente más de 75 orígenes comprimidos con códecs del Administrador de compresión de vídeo (VCM). Además, si el proyecto en su conjunto contiene más de 75 orígenes de este tipo, debe usar la reconexión dinámica o DES no puede obtener una vista previa del proyecto. Para obtener más información, [**vea IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**IamTimelineTrack (interfaz)**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





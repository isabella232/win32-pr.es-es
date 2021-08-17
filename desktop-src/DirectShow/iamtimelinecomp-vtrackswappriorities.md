---
description: El método VTrackSwapPriorities cambia los niveles de prioridad de dos pistas.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: Método IAMTimelineComp::VTrackSwapPriorities (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eb67e07f96ec2e8377690a5cd5233ba6cdb40242870da6d5f23b5f404b77b890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999288"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>Método IAMTimelineComp::VTrackSwapPriorities

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `VTrackSwapPriorities` método cambia los niveles de prioridad de dos pistas.

Dados dos niveles de prioridad, este método cambia las pistas virtuales en esas prioridades. Cuando el método vuelve, la pista que estaba en el primer nivel de prioridad está ahora en el segundo nivel de prioridad y viceversa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

Primer nivel de prioridad en el que se intercambian las pistas virtuales.

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

Segundo nivel de prioridad en el que se intercambian las pistas virtuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

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

 

 





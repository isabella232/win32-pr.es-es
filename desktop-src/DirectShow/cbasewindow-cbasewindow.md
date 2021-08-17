---
description: 'Constructor CBaseWindow.CBaseWindow: método constructor.'
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Constructor CBaseWindow.CBaseWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8873ee896d910d1596138a8d116c93ae0190534bac48b6ceb19165074f07b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016753"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Constructor CBaseWindow.CBaseWindow

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bDoGetDC* 
</dt> <dd>

Valor booleano que especifica si se debe recuperar el contexto del dispositivo.

</dd> <dt>

*bPostToDestroy* 
</dt> <dd>

Valor booleano que especifica la variable [**miembro CBaseWindow::m \_ bDoPostToDestroy.**](cbasewindow-m-bdoposttodestroy.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Después de crear el objeto , llame al [**método CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) para crear la ventana. **PrepareWindow** es un método virtual. Llama a [**CBaseWindow::InitialiseWindow,**](cbasewindow-initialisewindow.md)también un método virtual. Estos métodos están separados del constructor para que las clases derivadas puedan invalidarlos, si es necesario.

Si el valor del *parámetro bDoGetDC* es **TRUE,** el objeto recupera un identificador en el contexto de dispositivo (DC) de la ventana y lo almacena en la variable miembro `CBaseWindow` [**\_ hdc CBaseWindow::m.**](cbasewindow-m-hdc.md) El objeto también crea un controlador de dominio de memoria compatible, que almacena en la variable miembro [**CBaseWindow::m \_ MemoryDC.**](cbasewindow-m-memorydc.md) Estas acciones se producen en el **método InitialiseWindow.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 





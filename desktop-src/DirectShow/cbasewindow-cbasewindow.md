---
description: Método de constructor.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Constructor CBaseWindow. CBaseWindow (Winutil. h)
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
ms.openlocfilehash: a1741f8596210afac676a7e81f57b46e18fbba9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660236"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Constructor CBaseWindow. CBaseWindow

Método de constructor.

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

Valor booleano que especifica la variable miembro [**CBaseWindow:: m \_ bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Después de crear el objeto, llame al método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) para crear la ventana. **PrepareWindow** es un método virtual. Llama a [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md), también a un método virtual. Estos métodos se separan del constructor para que las clases derivadas puedan invalidarlos, si es necesario.

Si el valor del parámetro *bDoGetDC* es **true**, el `CBaseWindow` objeto recupera un identificador para el contexto de dispositivo (DC) de la ventana y lo almacena en la variable miembro [**CBaseWindow:: m \_ HDC**](cbasewindow-m-hdc.md) . El objeto también crea un controlador de dominio de memoria compatible, que almacena en la variable miembro [**CBaseWindow:: m \_ MemoryDC**](cbasewindow-m-memorydc.md) . Estas acciones se producen en el método **InitialiseWindow** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 





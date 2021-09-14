---
description: El método CreateEmptyNode crea un nuevo objeto de escala de tiempo.
ms.assetid: 64184bfd-6f93-4865-81e7-b1ed7b7148aa
title: Método IAMTimeline::CreateEmptyNode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.CreateEmptyNode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 894126bea8f40537602aa1fe8898038245215914
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266348"
---
# <a name="iamtimelinecreateemptynode-method"></a>IamTimeline::CreateEmptyNode (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `CreateEmptyNode` método crea un nuevo objeto de escala de tiempo.

Use este método para crear objetos de escala de tiempo, en lugar de la **función CoCreateInstance,** porque este método realiza rutinas de inicialización importantes. Cada objeto creado por este método admite al menos la [**interfaz IAMTimelineObj,**](iamtimelineobj.md) junto con otras interfaces específicas de ese tipo de objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateEmptyNode(
  [out] IAMTimelineObj      **ppObj,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IAMTimelineObj del nuevo**](iamtimelineobj.md) objeto.

</dd> <dt>

*Tipo* 
</dt> <dd>

Miembro del tipo [**enumerado TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) especificando el tipo de objeto que se creará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

No agregue el nuevo objeto a otra instancia de escala de tiempo. Cada objeto de una escala de tiempo debe crearse mediante esa escala de tiempo.

Si el método se realiza correctamente, la [**interfaz IAMTimelineObj**](iamtimelineobj.md) que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IamTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





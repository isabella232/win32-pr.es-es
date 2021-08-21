---
description: El método Remove quita este objeto de la escala de tiempo (incluidos los subobjetos, pero no los elementos secundarios), para su reinserción en otra parte.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: Método IAMTimelineObj::Remove (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356f7239cbdbe3972f11fcc95dd9bf44dc1b06d086a8e44c9131c0061f3ec211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155268"
---
# <a name="iamtimelineobjremove-method"></a>IAMTimelineObj::Remove (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método quita este objeto de la escala de tiempo (incluidos los subobjetos, pero no los elementos secundarios), para `Remove` su reinserción en otra parte.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Llame a este método solo si la aplicación volverá a insertar inmediatamente el objeto en la escala de tiempo. Es una operación no válida llamar a este método sin volver a reinsertar el objeto. Para quitar un objeto de forma permanente, llame [**a IAMTimelineObj::RemoveAll**](iamtimelineobj-removeall.md).

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

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





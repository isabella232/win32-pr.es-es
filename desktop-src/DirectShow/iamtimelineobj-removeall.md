---
description: El método RemoveAll quita permanentemente este objeto de la escala de tiempo, incluidos los subobjetos y los elementos secundarios.
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: Método IAMTimelineObj::RemoveAll (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 92bae081c5f888d271bfdeb278ca4c0d2b210fffddce8b57c76d5f446fc9e4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400753"
---
# <a name="iamtimelineobjremoveall-method"></a>IamTimelineObj::RemoveAll (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método quita permanentemente este objeto de la escala de `RemoveAll` tiempo, incluidos los subobjetos y los elementos secundarios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Para quitar un objeto con el fin de reinsertarlo en otro lugar de la escala de tiempo, llame a [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).

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

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





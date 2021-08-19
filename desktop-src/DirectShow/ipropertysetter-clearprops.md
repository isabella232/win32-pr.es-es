---
description: El método ClearProps borra todos los datos de propiedad del setter de propiedad. La aplicación puede establecer nuevos datos de propiedad después de llamar a esta función.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: Método IPropertySetter::ClearProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dfe5db4d7ae1f4a2d7a070a3d735264e61dfbdb621f99b9cbb2e1040213b56c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818594"
---
# <a name="ipropertysetterclearprops-method"></a>IPropertySetter::ClearProps (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `ClearProps` método borra todos los datos de propiedad del setter de propiedad. La aplicación puede establecer nuevos datos de propiedad después de llamar a esta función.

Borrar los datos de propiedad no restaura las propiedades del objeto a sus valores originales. Simplemente impide que DirectShow aplicar más cambios. Los valores de propiedad se aplican en tiempo de ejecución cuando se representa el proyecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

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

[**IPropertySetter (interfaz)**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





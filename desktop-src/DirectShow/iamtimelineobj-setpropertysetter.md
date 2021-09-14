---
description: El método SetPropertySetter establece el establecedor de propiedades del objeto. Cuando se representa el objeto, la información de propiedad contenida en el setter de propiedad se aplica al objeto . Llame a este método en objetos de transición y efecto.
ms.assetid: 3ce2fe50-a884-4da4-95b5-9c97e188f819
title: Método IAMTimelineObj::SetPropertySetter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cf8cea3abbcc25c91a398af1af61b0ff4de0cd5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160159"
---
# <a name="iamtimelineobjsetpropertysetter-method"></a>Método IAMTimelineObj::SetPropertySetter

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetPropertySetter` método establece el establecedor de propiedades del objeto. Cuando se representa el objeto, la información de propiedad contenida en el setter de propiedad se aplica al objeto . Llame a este método en objetos de transición y efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPropertySetter(
   IPropertySetter *newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
</dt> <dd>

Puntero a la interfaz [**IPropertySetter**](ipropertysetter.md) del setter de la propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

 

 





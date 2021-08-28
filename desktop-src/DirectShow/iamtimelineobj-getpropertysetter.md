---
description: El método GetPropertySetter recupera el setter de propiedades del objeto. Cuando se representa el objeto, la información de propiedad contenida en el setter de propiedad se aplica al objeto .
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: Método IAMTimelineObj::GetPropertySetter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd86d1c0b8334c1587745278ee499e38113887bb074770f49364429f71fa53da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831085"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>IamTimelineObj::GetPropertySetter (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetPropertySetter` método recupera el setter de propiedad del objeto. Cuando se representa el objeto, la información de propiedad contenida en el setter de propiedad se aplica al objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe un puntero a la interfaz [**IPropertySetter**](ipropertysetter.md) del setter de la propiedad. Si el objeto no tiene un establecedor de propiedades, el valor se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Si el valor devuelto en *pVal* no es **NULL,** la **interfaz IPropertySetter** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**IAMTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





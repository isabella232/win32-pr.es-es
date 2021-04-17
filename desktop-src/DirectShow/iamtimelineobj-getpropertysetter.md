---
description: El método GetPropertySetter recupera el establecedor de propiedad del objeto. Cuando se representa el objeto, la información de la propiedad contenida en el establecedor de propiedad se aplica al objeto.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'IAMTimelineObj:: GetPropertySetter (método) (QEDIT. h)'
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
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690759"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a>IAMTimelineObj:: GetPropertySetter (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetPropertySetter` método recupera el establecedor de propiedad del objeto. Cuando se representa el objeto, la información de la propiedad contenida en el establecedor de propiedad se aplica al objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe un puntero a la interfaz [**IPropertySetter**](ipropertysetter.md) del establecedor de propiedad. Si el objeto no tiene un establecedor de propiedad, el valor se establece en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si el valor devuelto en *pval* no es **null**, la interfaz **IPropertySetter** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineObj**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





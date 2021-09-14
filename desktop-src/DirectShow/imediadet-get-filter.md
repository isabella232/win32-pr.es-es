---
description: El método get \_ Filter recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: Método IMediaDet::get_Filter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886937"
---
# <a name="imediadetget_filter-method"></a>IMediaDet::get \_ Filter (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_Filter` método recupera un puntero al filtro de origen utilizado actualmente por el detector de medios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppVal* \[ out, retval\]
</dt> <dd>

Recibe un puntero a la interfaz **IUnknown del** filtro. Si no hay ningún filtro de origen en uso, el valor se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Cuando el método vuelve, si *\* ppVal* no es **NULL,** la **interfaz IUnknown** tiene un recuento de referencias pendiente. Libere la interfaz cuando haya terminado de usarlo.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





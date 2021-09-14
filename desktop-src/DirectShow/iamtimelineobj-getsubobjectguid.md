---
description: El método GetSubObjectGUID recupera el GUID del subobjeto asociado a este objeto de escala de tiempo.
ms.assetid: c2787e6b-ed72-4a6c-9e1e-c79c00020585
title: Método IAMTimelineObj::GetSubObjectGUID (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1c787bdbca8bbd255ccc78c3756fd0071d22f30d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061656"
---
# <a name="iamtimelineobjgetsubobjectguid-method"></a>Método IAMTimelineObj::GetSubObjectGUID

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `GetSubObjectGUID` método recupera el GUID del subobjeto asociado a este objeto de escala de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSubObjectGUID(
   GUID *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe el GUID del subobjeto o \_ GUID NULL si el objeto no tiene un subobjeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

[**IAMTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





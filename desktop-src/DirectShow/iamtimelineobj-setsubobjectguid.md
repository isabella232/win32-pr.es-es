---
description: El método SetSubObjectGUID especifica el GUID del subobjeto asociado a este objeto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: Método IAMTimelineObj::SetSubObjectGUID (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: faa87455b2b96e5a2ce2cae8f7662a205a9b9b4124033e95f8aa5c21ae26b745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316406"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a>Método IAMTimelineObj::SetSubObjectGUID

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetSubObjectGUID` método especifica el GUID del subobjeto asociado a este objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetSubObjectGUID(
   GUID newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
</dt> <dd>

GUID del subobjeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El motor de representación crea una instancia del subobjeto según sea necesario.

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

[**IAMTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





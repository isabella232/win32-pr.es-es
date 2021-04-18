---
description: El método SetSubObjectGUID especifica el GUID del subobjeto asociado a este objeto.
ms.assetid: 1f21e242-306e-4b28-8655-511b7db495ab
title: 'IAMTimelineObj:: SetSubObjectGUID (método) (QEDIT. h)'
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
ms.openlocfilehash: ac5e7631b447d28c92bc94cb64cfeabde0e6cd6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690717"
---
# <a name="iamtimelineobjsetsubobjectguid-method"></a>IAMTimelineObj:: SetSubObjectGUID (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

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

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El motor de representación crea una instancia del subobjeto según sea necesario.

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

 

 





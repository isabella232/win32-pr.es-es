---
description: El método SetGroupName establece el nombre definido por la aplicación del grupo.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: 'IAMTimelineGroup:: SetGroupName (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetGroupName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 327bf0384ce484353ac41c069ddf580c674b0b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690104"
---
# <a name="iamtimelinegroupsetgroupname-method"></a>IAMTimelineGroup:: SetGroupName (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetGroupName` método establece el nombre definido por la aplicación del grupo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetGroupName(
   BSTR pGroupName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGroupName* 
</dt> <dd>

**BSTR** que especifica el nombre del grupo. La longitud máxima del nombre es de 256 caracteres, incuding el terminador null.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

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

[**Interfaz IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





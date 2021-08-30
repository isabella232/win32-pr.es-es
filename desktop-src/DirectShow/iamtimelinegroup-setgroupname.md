---
description: El método SetGroupName establece el nombre definido por la aplicación del grupo.
ms.assetid: e1d8a91b-d5b9-42a4-9b98-582e1a57ac51
title: Método IAMTimelineGroup::SetGroupName (Qedit.h)
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
ms.openlocfilehash: cf9b80c74c85b335770b6ae0e922d7cc24246b88ab8e7fb7e2b74c396b927a1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965125"
---
# <a name="iamtimelinegroupsetgroupname-method"></a>IamTimelineGroup::SetGroupName (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

**BSTR** que especifica el nombre del grupo. La longitud máxima del nombre es de 256 caracteres, incluido el terminador nulo.

</dd> </dl>

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

[**IAMTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método SetUserData establece datos persistentes definidos por la aplicación.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: Método IAMTimelineObj::SetUserData (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c136be271e5ef34423096a807e833ca5e3f3eb5412a4938d8750400cd1a88902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154944"
---
# <a name="iamtimelineobjsetuserdata-method"></a>IamTimelineObj::SetUserData (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetUserData` método establece datos persistentes definidos por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Puntero a un búfer que contiene los datos.

</dd> <dt>

*Tamaño* 
</dt> <dd>

Tamaño de los datos, en bytes.

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

[**IamTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





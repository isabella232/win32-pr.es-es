---
description: El método SetUserName establece un nombre definido por la aplicación para el objeto .
ms.assetid: 6f071884-519a-465f-8273-ab1be58dda8b
title: Método IAMTimelineObj::SetUserName (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ec39aece23d38be6fbe2e69f7ded8bc738e04c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061634"
---
# <a name="iamtimelineobjsetusername-method"></a>IamTimelineObj::SetUserName (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetUserName` método establece un nombre definido por la aplicación para el objeto .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetUserName(
   BSTR newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* 
</dt> <dd>

Cadena de caracteres anchos que contiene el nombre. Las cadenas de más de 256 caracteres pueden truncarse.

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

 

 





---
description: El método WriteXML convierte una escala de tiempo en una cadena XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: Método IXml2Dex::WriteXML (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061061"
---
# <a name="ixml2dexwritexml-method"></a>IXml2Dex::WriteXML (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `WriteXML` método convierte una escala de tiempo en una cadena XML.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntero a la interfaz **IUnknown** del objeto de escala de tiempo.

</dd> <dt>

*pbstrXML* 
</dt> <dd>

Puntero a una variable de tipo BSTR que recibe la cadena XML que describe la escala de tiempo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente. Si no hay memoria suficiente para la conversión, devuelve E \_ OUTOFMEMORY. De lo contrario, devuelve otro código de error.

## <a name="remarks"></a>Observaciones

El método asigna memoria para la cadena. La aplicación debe llamar **a SysFreeString para** liberar la memoria.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4.0 o posterior<br/>                                               |
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IXml2Dex (interfaz)**](ixml2dex.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





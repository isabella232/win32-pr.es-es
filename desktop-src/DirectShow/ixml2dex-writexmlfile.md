---
description: El método WriteXMLFile traduce una escala de tiempo a XML y escribe los datos XML en un archivo.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex:: WriteXMLFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690909"
---
# <a name="ixml2dexwritexmlfile-method"></a>IXml2Dex:: WriteXMLFile (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `WriteXMLFile` método traduce una escala de tiempo a XML y escribe los datos XML en un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Puntero a la interfaz **IUnknown** del objeto Timeline.

</dd> <dt>

*FileName* 
</dt> <dd>

Cadena que especifica el nombre del archivo que se va a escribir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación de la interfaz. **HRESULT** puede incluir una de las siguientes constantes estándar u otros valores que no se muestran en la lista.



| Código devuelto                                                                                   | Descripción                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El argumento no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>             |



 

## <a name="remarks"></a>Observaciones

Este método genera un archivo XML que representa todos los componentes de la escala de tiempo.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Internet Explorer 4,0 o posterior<br/>                                               |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IXml2Dex**](ixml2dex.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 





---
description: El método WriteGrfFile escribe un gráfico de filtro en un archivo en formato. GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex:: WriteGrfFile (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690461"
---
# <a name="ixml2dexwritegrffile-method"></a>IXml2Dex:: WriteGrfFile (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `WriteGrfFile` método escribe un gráfico de filtro en un archivo en formato. GRF.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Puntero a la interfaz **IUnknown** del gráfico de filtro.

</dd> <dt>

*FileName* 
</dt> <dd>

Cadena que especifica el nombre del archivo que se va a escribir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que depende de la implementación de la interfaz. HRESULT puede incluir una de las siguientes constantes estándar u otros valores que no se muestran en la lista.



| Código devuelto                                                                                  | Descripción                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Error.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El argumento no es válido.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>             |



 

Este método también puede devolver códigos de error generados por llamadas internas a los métodos **IStorage:: CreateStream (** y **IPersist:: Save** . Para obtener más información, vea el SDK de la plataforma.

## <a name="remarks"></a>Observaciones

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

 

 





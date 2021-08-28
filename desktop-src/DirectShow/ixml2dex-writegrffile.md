---
description: El método WriteGrfFile escribe un gráfico de filtro en un archivo en formato .grf.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: Método IXml2Dex::WriteGrfFile (Qedit.h)
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
ms.openlocfilehash: 121d901bee9da9b8ea6f7dad31e589002c0b4859619f6dd02941f438af3b647f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767025"
---
# <a name="ixml2dexwritegrffile-method"></a>IXml2Dex::WriteGrfFile (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `WriteGrfFile` método escribe un gráfico de filtro en un archivo en formato .grf.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pgraph* 
</dt> <dd>

Puntero a la interfaz **IUnknown** del gráfico de filtros.

</dd> <dt>

*FileName* 
</dt> <dd>

Cadena que especifica el nombre del archivo que se debe escribir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que depende de la implementación de la interfaz . HRESULT puede incluir una de las siguientes constantes estándar u otros valores no enumerados.



| Código devuelto                                                                                  | Descripción                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Error.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El argumento no es válido.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>             |



 

Este método también puede devolver códigos de error generados por llamadas internas a los métodos **IStorage::CreateStream** **e IPersist::Save.** Para obtener más información, consulte el SDK de plataforma.

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Internet Explorer 4.0 o posterior<br/>                                               |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IXml2Dex (interfaz)**](ixml2dex.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 





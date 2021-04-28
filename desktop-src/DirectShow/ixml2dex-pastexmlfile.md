---
description: 'Método IXml2Dex::P asteXMLFile: no implementado.'
ms.assetid: 25300ba5-3578-4eb3-99e2-d547dbb2b9ee
title: Método IXml2Dex::P asteXMLFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.PasteXMLFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: 415e71d87d8e8d9c7834df0a16fce754651d6a03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088963"
---
# <a name="ixml2dexpastexmlfile-method"></a>Método IXml2Dex::P asteXMLFile

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Sin implementar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PasteXMLFile(
   IUnknown *pTimeline,
   double   dStart,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Reservado.

</dd> <dt>

*dStart* 
</dt> <dd>

Reservado.

</dd> <dt>

*FileName* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la Microsoft Windows SDK [update para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IXml2Dex (interfaz)**](ixml2dex.md)
</dt> </dl>

 

 




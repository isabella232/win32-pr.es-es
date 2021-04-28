---
description: 'Método IXml2Dex::CreateGraphFromFile: no implementado.'
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: IXml2Dex::CreateGraphFromFile (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.CreateGraphFromFile
api_type:
- COM
api_location: ''
ms.openlocfilehash: a79b4115dddb0e15adb4284bbefd245aba088d5f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084423"
---
# <a name="ixml2dexcreategraphfromfile-method"></a>IXml2Dex::CreateGraphFromFile (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Sin implementar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateGraphFromFile(
   IUnknown **ppGraph,
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppGraph* 
</dt> <dd>

Reservado.

</dd> <dt>

*pTimeline* 
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

 

 




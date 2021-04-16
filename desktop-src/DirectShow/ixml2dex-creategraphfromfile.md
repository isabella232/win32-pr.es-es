---
description: Sin implementar.
ms.assetid: b476e0c9-1432-4644-8002-154797a2a594
title: 'IXml2Dex:: CreateGraphFromFile (método)'
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
ms.openlocfilehash: 10a2e52716de77f9c62a51c87cbda550b92a8f90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686314"
---
# <a name="ixml2dexcreategraphfromfile-method"></a>IXml2Dex:: CreateGraphFromFile (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

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

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IXml2Dex**](ixml2dex.md)
</dt> </dl>

 

 




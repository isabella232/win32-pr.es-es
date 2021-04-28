---
description: 'Método IRenderEngine::SetInterestRange: no compatible.'
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: IRenderEngine::SetInterestRange (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084463"
---
# <a name="irenderenginesetinterestrange-method"></a>IRenderEngine::SetInterestRange (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

No compatible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Reservado.

</dd> <dt>

*Detención* 
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

[**IRenderEngine (interfaz)**](irenderengine.md)
</dt> </dl>

 

 




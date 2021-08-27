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
ms.openlocfilehash: d462ed73680d27daa476d653c2d08935c40ba4b26bddce93c9baf8246c9cb581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083675"
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
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRenderEngine (interfaz)**](irenderengine.md)
</dt> </dl>

 

 



